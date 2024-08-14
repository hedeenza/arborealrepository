---
title: Rower Hometown Map - pt.1
author: Zach Hedeen
date: '2024-08-14'
slug: rower-hometown-map-pt-1
categories:
  - Projects
tags:
  - Coding
  - R
  - Rowing
  - Visualization
---

# Introduction 

&emsp; An important part of building a continually successful rowing team - or any team with turnover for that matter -  is strategic recruitment. If you don't have high quality people coming in as your previous high quality people leave, you're going to be in a tough spot. Many Division 1 teams in the United States recruit from all across the country and internationally to find the talent that will help their team continue their storied legacy of excellence. 
&emsp; I thought it would be interesting to visualize the areas Division 1 rowing teams are recruiting from to see if there are any patterns. A full sense of the scope of recruitment practices across many years may help identify:

- Changes in the areas athletes have been recruited over time.
- Differences in recruitment practices between universities or conferences.
- Areas that may be producing high quality rowing talent, but are not being examined as closely. 

&emsp; My goal by the end of this is to have an interactive map that users can examine while manipulating variables like year and conference. Many of the skills are beyond my current ability, but the framework of this project will help guide me to acquiring the skills I need. 

# Building a Web-Scraper

&emsp; For a list of links, the scraper should be able to pull roster data and append that data to the end of a table. To perform this in R, I used the {rvest} package. 

```
library(tidyverse)
library(rvest)
```

&emsp; First I needed to find a URL:

```
# Assign the URL
url <- "https://osubeavers.com/sports/mens-rowing/roster"
```
&emsp; Using rvest::read_html(url) I was able to scrape the web-page information that I needed. 

```
# Reading the HTML
html_source <- read_html(url)
```

&emsp; Past web-scraping projects have had their challenges, but with this one it almost seemed like the data wasn't getting loaded in. I went back and used the rvest::html_text() function to determine whether or not content had in fact been pulled. Once I ran this, it was clear the content made it into R.

```
# The HTML actually got read in 
html_source %>% html_text()
```
&emsp; Inspecting the web page I was able to navigate to the proper node to grab the roster table information. Don't mind the messy name. It took a couple tries. 

```
# Which section of the page will go to the table
css_test_2 <- ".c-rosterpage__content"
```
# If At First You Don't Succeed...

&emsp; Likely due to a page formatting issue, I was unable to use rvest::html_table() like I have in the past. Unfortunately I would need to do a lot of manipulation by hand in order to make a tidy table. I used rvest:: html_text2() because it resulted in the line breaks displaying as "\n" which I could use to split the text into multiple lines.

```
# Extracting the text, because the table function isn't functioning
# html_text2() to insert the \n at line breaks to help ease the next steps
tester <- html_nodes(html_source, css_test_2) %>% html_text2()

# Splitting on the line breaks
paragraphs <- tester %>% str_split("\n")
```

&emsp; Manipulation with {stringr} requires a vector, so I coerced it. Don't ask how long it took me to realize that that's what the problem was. 

```
# Coerce to vector to allow work with {stringr}
df <- as_vector(paragraphs)
```
&emsp; Though the lines were Separated by line break, I realized many of them had run together. I used Regex commands to detect the lower-case letter running into the upper-case letter. Running this let me know that R could see what I was going after. 

```
# Can detect the pattern 
str_detect(df, "[:lower:][:upper:]")
```

&emsp; With that green light, I began creating line breaks in the text to allow me to separate the text in the cells into their own cells. "\\1" and "\\2" are used to reference the first and second item that were detected. 

```
# Make a line break between the mashed together lower case and upper case values in adjacent columns
str_replace_all(df, "([:lower:])([:upper:])", "\\1 \n \\2") |>
# Make a line break between the mashed together period and upper case values in adjacent columns
str_replace_all("([:punct:])([:upper:])", "\\1 \n \\2") |>
# Split into their own cells
str_split("\n") |>

as_vector() |>
head()
```
&emsp; The test ran well, so I went ahead and assigned in to a variable. I removed all of the text that will eventually go into the column names and trimmed off the white space on both sides. 

```
# Detecting the cells running together, inserting a line break between them, separating into their own rows
clean_df <- 
  str_replace_all(df, "([:lower:])([:upper:])", "\\1 \n \\2") |>
  str_replace_all("([:punct:])([:upper:])", "\\1 \n \\2") |>
  str_split("\n") |>
  as_vector() |>
str_remove_all('Name|Position|Academic Year|Height|Hometown|Last School') |>
  str_trim(side = "both") |>
  as_vector() |>
  print()
```
&emsp; That's when I realized something was wrong. It didn't look right. I saw that there was a "Full Bio" column so I used {stringr} to detect it. That's when I saw that there were unequal numbers of "FALSE" values between each "TRUE" where the Full Bio cells were. There were missing values. I looked back at the table on the website and indeed, that was the case. 

```
# Oh no... not everyone has the same amount of information...
str_detect(clean_df, "Full Bio")
```
**Always take a careful look at what you're scraping before you commit to a plan of action.**

# ... Try, Try Again

&emsp; Next I decided to try without the line breaks ("\n") provided by rvest::html_text2().

```
# Well there's different amounts of information on everyone, but there's always a FULL BIO link,
tester_2 <- html_nodes(html_source, css_test_2) %>% html_text()
```
&emsp; I realized that because there was a FULL BIO section at the end of the original line for each athlete, even if they were missing other data, I decided to use that as a marker to create my rows.

```
in_rows <- 
  tester_2 |>
  
  # Separate run togethers of punctuation and upper case
  str_replace_all("([:punct:])([:upper:])", "\\1 \\2") |>
  
  # Separate run-togethers of lower and upper
  str_replace_all("([:lower:])([:upper:])", "\\1 \\2") |>
  
  # Replacing the FULL BIO FOR "FIRST" "LAST" with a line break, because that's always present, 
    grabbing the next two full words, which are the athlete's first and last, also always present
  str_replace_all("Full Bio  for \\w+ \\w+", " \n") |>
  
  # Splitting each athlete into their own line
  str_split("\n") |>
  
  # Coercing to vector to continue work 
  as_vector() |>
  
  # Removing the blank space from the sides
  str_trim(side = "both") |>
  
  # Removing the category names
  str_remove_all("Position|Academic Year|Height|Hometown|Last School") |>
  
  # Removing errant white space in the middle
  str_squish() |>
  print()
```
&emsp; Looking at the printed data, I could see that there were a couple errors specific to the scraped data. Getting those cleared was next.

```
specific_errors <-
  in_rows |>
  # Removing a single error caused by a hyphenated last name
  str_replace_all("- Hull Sasha Herrmann", "Sasha Herrman") |>
  # Removed another individual name case
  str_remove_all("Custom Field 1Ethan de Borja") |>
  print()
```  
&emsp; Now the fun step. I needed to come up with a way to widen the data. Thankfully there's tidyr::separate_wider_delim(). With the data as it was, there's no clean way to widen as I desired, so I used {stringr} functions to add a chosen delimiter, "*", where I wanted the breaks between columns to be. 
  
```
delim_add <-
  specific_errors |>
  # Adding custom delimiters between values that will feed into each column
  str_replace_all(" Rower ", "*Rower*") |>
  str_replace_all(" Coxswain ", "*Coxswain*") |>
  
  # There was a space between the N. H. for New Hampshire, which first needed to be collapsed
  str_replace_all("\\. [:upper:]\\.", '.H.') |>
  
  # Adding the delimiter after the academic year
  str_replace_all("\\. ", "\\.*") |>
  
  # Adding the delimiter after the height
  str_replace_all("\'' ", "\''*") |>
  
  as.data.frame() |>
  print()
```

&emsp; The name of the single column was messy, so I cleaned it to make it easier to work with tidyr::separate_wider_delim()

```
names(delim_add) <- "Athletes"

wide_roster <-
  delim_add |>
  separate_wider_delim(
    delim = "*",
    cols = Athletes,
    names = c("Name", "Position", "Acacdemic Year", "Height", "Hometown", "Last School"),
    too_few = 'align_start')
```

&emsp; All that was left was to add some additional information as to which team the data came from so groups could be assigned when the master, combined table would eventually be created. 

```
roster_tags <-
  wide_roster |>
  mutate(University = "OSU", 
         Team = "Men",
         Year = "2023-2024")
```

# Automated Scraper

&emsp; Now that the data could be scraped and tidied, it was time to put it in some kind of automation. I used a for loop. I assigned the links to a vector, then created a "blank" data frame the scraper could fill in.

```
# Oregon State University - FUNCTIONS 
osu_links <- c("https://osubeavers.com/sports/mens-rowing/roster",
               "https://osubeavers.com/sports/womens-rowing/roster")
osu_roster <- data.frame(0, 0, 0, 0, 0, 0)
  names(osu_roster) = c("Name", "Position", "Acacdemic-Year", "Height", "Hometown", "Link")
```

&emsp; Here's the full for loop

```
# OSU Scraper - for loop
for (squad in osu_links) {    # for each link in the links vector
  url <- squad                # assign the url
  html <- read_html(url) |>   # scrape the page
    html_nodes(".c-rosterpage__content") |>
    html_text() |> 
    str_replace_all("([:punct:])([:upper:])", "\\1 \\2") |>   # Do all of the tidying work from the stages before
    str_replace_all("([:lower:])([:upper:])", "\\1 \\2") |>
    str_replace_all("Full Bio  for \\w+ \\w+", " \n") |>
    str_split("\n") |>
    as_vector() |>
    str_trim(side = "both") |>
    str_remove_all("Position|Academic Year|Height|Hometown|Last School") |>
    str_squish() |>
    str_replace_all("- Hull Sasha Herrmann", "Sasha Herrman") |>
    str_remove_all("Custom Field 1Ethan de Borja") |>
    str_replace_all(" Rower ", "*Rower*") |>
    str_replace_all(" Coxswain ", "*Coxswain*") |>
    str_replace_all("\\. [:upper:]\\.", '.H.') |>
    str_replace_all("\\. ", "\\.*") |>
    str_replace_all("\'' ", "\''*") |>
    as.data.frame()
  
  names(html) <- "Athletes"       # Clean the name
  
  wide_roster <-        # Widen the data
    html |>
    separate_wider_delim(
      delim = "*",
      cols = Athletes,
      names = c("Name", "Position", "Acacdemic-Year", "Height", "Hometown", "Last-School"),
      too_few = 'align_start',
      too_many = "drop")
  
  roster_tags <-        # Add the additional data
    wide_roster |>
    select(Name, Position, `Acacdemic-Year`, Height, Hometown) |>
    mutate(Link = squad)
  
  osu_roster <- rbind(osu_roster, roster_tags)        # Bind the rows you process to the growing table
  
  print(paste("Done:", squad))        # Let us know you're done with each loop
}
```

&emsp; Lastly, I wrote the data to a local csv so the next time I pick this up I don't have to harass their website. 
```
# Writing the roster data to a local csv
write_csv(osu_roster, "Data/osu_roster.csv")
```
&emsp; The data is a little messy due to some missing values in the womens team roster, but it's nothing some persistence can't clean. 

# When It's the Same but Not

&emsp; Most D1 university rowing team websites appear almost identical. When I started this project I thought it would be a simple matter of pasting in additional links to the vector and running the loop. This was not the case. 

&emsp; I tried to run all of the former PAC12 Division 1 team rosters, but wound up with only 94 athletes getting their data loaded. Putting the links into smaller batches revealed that the scraping loop as is worked for a couple of teams, but not *at all* for others. Inspecting the University of Washington page source code revealed that while the aesthetic is similar to the Oregon State University page, the underlying architecture is just different enough that the scraper tool will need to be tweaked in order to get the information I'm after. 

&emsp; The tweaks needed to import the data from the other rosters, importing the other rosters, and potential next steps will be the subject of the next post for this project. 

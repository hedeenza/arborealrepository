---
title: 'Critical Role: The Almost Impossible (Campaign 1 - Vox Machina)'
author: Zach Hedeen
date: '2024-08-14'
slug: critical-role-the-almost-impossible-campaign-1
categories:
  - Projects
tags:
  - R
  - Critical Role
  - DnD
output:
  html_document: 
    toc: TRUE
    toc_depth: 2
    toc_float: TRUE
---
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/kePrint/kePrint.js"></script>
<link href="{{< blogdown/postref >}}index_files/lightable/lightable.css" rel="stylesheet" />

&emsp; *This is a repost of a previous project originally from 15 June 2024.* 



<style type="text/css">
pre {
  max-height: 300px;
  overflow-y: auto;
}

pre[class] {
  max-height:225px;
}
</style>

# 1. Introduction

&emsp; [Critical Role](https://critrole.com/) is a series in which a star-studded cast of Hollywood voice actors play Dungeons & Dragons. It's a story known for its length (and you thought catching up on the Marvel Cinematic Universe was bad):

<table class="table" style="margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; " colspan="5"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Critical Role Run Time in Context</div></th></tr>
  <tr>
   <th style="text-align:center;"> Campaign </th>
   <th style="text-align:center;"> Start Date </th>
   <th style="text-align:center;"> End Date </th>
   <th style="text-align:center;"> Play Time </th>
   <th style="text-align:center;"> # of 45' Cable TV Episodes </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;"> 1 - Vox Machina </td>
   <td style="text-align:center;"> March 2015 </td>
   <td style="text-align:center;"> October 2017 </td>
   <td style="text-align:center;"> 373 hours 23 minutes </td>
   <td style="text-align:center;"> 497.8 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 2 - The Mighty 9 </td>
   <td style="text-align:center;"> January 2018 </td>
   <td style="text-align:center;"> June 2021 </td>
   <td style="text-align:center;"> 483 hours 40 minutes </td>
   <td style="text-align:center;"> 644.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 3 - Bell's Hells </td>
   <td style="text-align:center;"> October 2021 </td>
   <td style="text-align:center;"> Present (as of e95) </td>
   <td style="text-align:center;"> 351 hours 3 minutes </td>
   <td style="text-align:center;"> 468.1 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Other </td>
   <td style="text-align:center;"> June 2021 </td>
   <td style="text-align:center;"> June 2022 </td>
   <td style="text-align:center;"> 56 hours 46 minutes </td>
   <td style="text-align:center;"> 75.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> Total </td>
   <td style="text-align:center;"> March 2015 </td>
   <td style="text-align:center;"> Present </td>
   <td style="text-align:center;"> 1,265 hours 1 minute </td>
   <td style="text-align:center;"> 1,686.5 </td>
  </tr>
</tbody>
</table>

&emsp; And that's without the ads or mid-session break! It was only thanks to the ability to adjust the playback speed to 2.5x that I was able to catch up over the course of a year and a half. It's a story also known for its deep world building, poignant moments, celebrity guests (including Felicia Day, Joe Manganiello, Stephen Colbert, and Vin Diesel), and extremely dedicated fans. One fan, Stuart [Langridge](https://www.kryogenix.org/days/archives/), went so far as to build a [website](https://www.kryogenix.org/crsearch/) that has searchable transcripts of every episode, linked to the time stamp they occurred in their YouTube upload.

&emsp; During the game, players will roll one or more of several different types of dice and then add or subtract values related to their character and the conditions their in. If the roll is equal or greater to an assigned threshold, they are able to perform their intended action, and will sometimes roll again to determine the degree of effect of that action. Dungeons & Dragons lists several standard "Difficulty Classes" depending on how challenging the proposed action is. The values range from "Very Easy" at 5 to "Medium" at 15 to "Very Hard" at 25.

&emsp; But it's the very highest level that I want to focus on today: the "Nearly Impossible."

> &emsp; "In the general breakdown of difficulty classes... 30 is the top success level that they list. They don't list any higher than 30."
>
<footer>Brennan Lee Mulligan, [Exandria Unlimited: Calamity](https://youtu.be/KlIkkeWmVvA?si=WnsJlep0S02dzZTS&t=5976)</footer>

&emsp; When a player rolls 30 or higher on a 20-sided dice (including any appropriate modifiers) it is a notable occasion. I wanted to know how frequent these rolls were, who was rolling this high, and when these moments were happening during Campaign 1. Because this was a simple exploration of the data, it would only require a few often used packages.


``` r
library(tidyverse)
library(stringr)
library(kableExtra) # For the tables
```

---

# 2. Dataset

&emsp; The [dataset](https://docs.google.com/spreadsheets/d/1OEg29XbL_YpO0m5JrLQpOPYTnxVsIg8iP67EYUrtRJg/edit?gid=1355947030#gid=1355947030) was created by the hard work of the people at [CR Stats.](https://www.critrolestats.com/stats/) Thanks to Andrew K., Singing Badger, Lauren K., and Katherine K. for they work they've done compiling this and *so* much more data. While this team is retired, their work archiving the numbers is being continued by the team at [The Omen Archive](https://www.omenarchive.com/), though it unfortunately does seem they have not been cataloging every single roll. 

&emsp; First thing was to load the data. Unlike some other projects I've worked on, there was no need to skip any rows in order for the values to find themselves in the right places.



``` r
# Load Data
VM_Rolls <- read.csv("Data/Critical_Roll/VM_AllRolls.csv", skip = 0)
```

Episode, Time, Character, Type.of.Roll, Total.Value, Natural.Value, Crit., Damage, X..Kills, Notes

&emsp; Some of the names weren't the most readable for me, so I changed the ones I would be focusing on to something that would work going forward. 


``` r
# Renaming Columns
names(VM_Rolls)[4] <- "Roll_Type"
names(VM_Rolls)[5] <- "Total"
```



&emsp; Now that the data frame was workable, it was time to get a sense of what I was working with.

```
# How Many Rolls Were There?
nrow(VM_Rolls)    # 13,514
```
&emsp; 13,514 rolls is a lot of rolls, even for 337 hours 22 minutes and 38 seconds of game time (Thank you again CR Stats Team!) 

---

# 3. Cleaning

&emsp; Throughout the cleaning process I used to the following form to examine where there may have been input errors.

```
# Looking at what may be wrong
  table(VM_Rolls$TargetColumn) %>% as.data.frame() %>% arrange(Var1)
```

### 3.1. Episodes

&emsp; Most of the episode names were in a workable format. A few of the episodes were broken into a "Part 1" and a "Part 2." Thankfully, the `{stringr}` package made replacing these with a format that could be coerced into numeric for further processing quite simple. 


``` r
# Episodes 
  # Replacing the "parts" with decimals
  Episode_Clean_1 <- str_replace(VM_Rolls$Episode, "p1", ".1")
  Episode_Clean_2 <- str_replace(Episode_Clean_1, "p2", ".2")

  # Removing the space
  Episode_Clean_3 <- str_replace_all(Episode_Clean_2, pattern = " ", repl = "")

  # Coercing the episodes to numeric
  Episode_Final <- as.numeric(Episode_Clean_3) # 13,514
```


### 3.2. Timestamps

&emsp; I was worried about letter typos in the Time Stamps that would prevent their sorting. `{stringr}` allowed for a quick check.


``` r
# Time Stamps
  # Testing for non-time values
  Time_Test <- VM_Rolls %>% mutate(Letters = str_count(VM_Rolls$Time, "[:alpha:]"))
  
  # Checking, None Found
  # Time_Test %>% filter(Letters != 0)
  
  # Finalizing
  Time_Final <- VM_Rolls$Time
```

### 3.3. Character Attribution

&emsp; To accurately determine which characters performed which action, there needed to be accurate counts. There were a couple typos that separated the rolls attributed by each character into two groups. `{stringr}` saved the day again. 


``` r
# Which Character Rolled
  # Replacing the Tibierus and PIke typos
  Character_Clean_1 <- str_replace(VM_Rolls$Character, "Tibierus", "Tiberius")
  Character_Final <- str_replace(Character_Clean_1, "PIke", "Pike")
```

### 3.4. Roll Type

&emsp; Roll type had perhaps the greatest variability. Several entries essentially said the same thing but were worded a little differently. They were combined into one group to allow for more accurate counts. 


``` r
# Roll Type
  # Replacing Typos
  Roll_Type_Clean_1 <- str_replace_all(VM_Rolls$Roll_Type, "Steath", "Stealth")
  Roll_Type_Clean_2 <- str_replace_all(Roll_Type_Clean_1, "Beard Check", "Beard")
  Roll_Type_Clean_3 <- str_replace_all(Roll_Type_Clean_2, "Dex Save", "Dexterity Save")
  Roll_Type_Clean_4 <- str_replace_all(Roll_Type_Clean_3, "Wisdom Saving", "Wisdom Save")
  Roll_Type_Clean_5 <- str_replace_all(Roll_Type_Clean_4, "d100", "Percentile")
  Roll_Type_Final <- str_replace_all(Roll_Type_Clean_5, "Ressurection Roll", "Resurrection Roll")
```


### 3.5. Roll Total

&emsp; There were several different ways roll totals were reported. Because the total number was the focus, it wasn't important whether it was a Natural 20 or whether the value was exact. Using `stringr` the unnecessary parts were pulled off, anything that wasn't a number was replaced with an "NA," and any errant spaces were removed before the column was converted into numeric for later processing. 


``` r
# Roll Totals
  # Removing what we don't want, then replacing ambiguity with NA
  Total_Clean_1 <- str_replace_all(VM_Rolls$Total, "Natural|Nat|20=|1=|\\+|ish|\\<|\\>|\\?|18,", "")
  Total_Clean_2 <- str_replace_all(Total_Clean_1, "--|Unkknown|Unnknown|unknown|Unknown|N/A|Success|Misfire|Fail", "NA")
  Total_Clean_3 <- str_squish(Total_Clean_2)
  
  # Coercing to numeric
  Total_Final <- as.numeric(Total_Clean_3) # 13,514
```

### 3.6. Natural Roll

&emsp; The process for the Natural Rolls (the roll on the dice before any modifiers are accounted for) was similar to the processing for the totals. 


``` r
# Natural Roll Values
  # Removing what we don't want, then replacing ambiguity with NA
  Natural_Clean_1 <- str_replace_all(
                        VM_Rolls$Natural, "--|#REF!|Uknown|unknown|Unknown|Unkown", "NA")
  
  # Coercing to numeric
  Natural_Final <- as.numeric(Natural_Clean_1) # 13,514
```

### 3.7. Critical Indicator

&emsp; Rolling 20 on a 20 sided die is considered a "Critical Success," where the action not only succeeds but there is often additional positive effects. Rolling a 1 on a 20 sided die is considered a "Critical Fail," where the action not only fails but there is often some sort of additional negative consequence. There are other conditions, often in combat, that can end up being "critical." Whether it was a success, failure, or something else, I wanted to make sure that any ambiguous markings ("--") were replaced with something easier to work with. 


``` r
# Is It A Critical?
  # Removing what we don't want, then replacing ambiguity with NA
  Crit_Clean_1 <- str_replace_all(VM_Rolls$Crit., "--", "NA")

  # Coercing to numeric
  Crit_Final <- as.numeric(Crit_Clean_1) # 13,514
```

### 3.8. Kill Count

&emsp; Whether the attack roll resulted in the enemy's demise. A simple removal of some indications of ambiguity. 



``` r
# Kill Count
  # Fixing the ?
  Kills_Clean_1 <- str_replace_all(VM_Rolls$Kills, "\\?", "NA")

  # Coercing into numeric
  Kills_Final <- as.numeric(Kills_Clean_1) # 13,514
```

### 3.9. Rejoining the Cleaned Data  

&emsp; Now that all of the data has been cleaned, it was time to reassemble. 


``` r
# Rejoining the Data
  VM_Clean <- data.frame(Episode_Final, Time_Final, Character_Final, Roll_Type_Final, 
                       Total_Final, Natural_Final, Crit_Final, Kills_Final)
```

---

# 4. Adding Context

&emsp; The information contained is critical, but it's not the full story. For later analysis comparing Campaign 1 and Campaign 2 as well as indicate who was a member of the core party, additional data needed to be included. Further, when exploring the context of these high rolls, it's important to know not only the Roll Type (Skill, Save, Check, Attack, Damage, etc.) but also what core ability score it's associated with. 

> &emsp; Each of a creature's abilities has a score, a number that defines the magnitude of that ability. An **ability score** is not just a measure of innate capabilities, but also encompasses a creature's training and competence in activities related to that ability.
>
<footer>[Basic Rules](https://www.dndbeyond.com/sources/basic-rules/using-ability-scores#AbilityScoresandModifiers), Dungeons and Dragons</footer>

```
VM_Campaign <- VM_Clean %>% 
                mutate(Campaign = "1", 
                      Party = "Vox Machina",
                      Main_Party = case_when(Character_Final == "Arkhan" ~ FALSE,
                                             Character_Final == "Doty" ~ FALSE, ... 
                      Ability = case_when(Roll_Type_Final == "Athletics" ~ "Strength",
                                          Roll_Type_Final == "Strength" ~ "Strength", ...
                                    
```

&emsp; There was some ambiguity or it was outright unknown what ability score or skill a certain roll was associated with. The following is my best attempt at aligning roll types with their appropriate ability scores. 



### 4.1 Sorting Skills into their Abilities


``` r
# Number of Rolls of each Ability 
Ability_Count <- table(VM_Campaign$Ability) %>% 
                  as.data.frame() %>% 
                  arrange(factor(Var1, levels = c('Strength','Dexterity','Constitution',
                                                  'Intelligence','Wisdom','Charisma','Other'))) %>%
                  mutate("% of Total" = round((Freq/13509)*100,1))
      # Strength = 735
      # Dexterity = 2,792
      # Constitution = 591
      # Intelligence = 1,085
      # Wisdom = 1,871
      # Charisma = 500
      # Other = 5,935
names(Ability_Count) <-c("Ability", "Rolls", "% of Total")

Ability_Count_sOther <- table(VM_Campaign$Ability) %>% 
                          as.data.frame() %>% filter(Var1 != "Other") %>%
                          arrange(factor(Var1, levels = c('Strength','Dexterity','Constitution',
                                                          'Intelligence','Wisdom','Charisma','Other'))) %>%
                          mutate("% of Total" = round((Freq/7574)*100,1))

names(Ability_Count_sOther) <-c("Ability", "Rolls", "% of Total")
Ability_sOther_Final <- rbind(Ability_Count_sOther, c("1", "1", "1"))

# Top Number of Rolls by Type
# table(VM_Campaign$Roll_Type_Final) %>% as.data.frame() %>% arrange(desc(Freq))
      # Attack Rolls = 3,147
      # Damage Rolls = 2,161
      # Combat = 5,308 (of the 5,935)
      # Initiative Rolls = 688 (of the 2,792)

# Skill by Ability Table
Skill_Ability_Table <- VM_Campaign %>% 
                        select(Ability, Roll_Type_Final) %>% 
                        unique() %>% 
                        distinct(.keep_all = T) %>% 
                        filter(!is.na(Ability)) %>%
                        arrange(Ability)
              
# Adding a Counter Column to allow Pivoting Wider
Skill_Ability_Sorted <- Skill_Ability_Table %>% 
                          group_by(Ability) %>% 
                          arrange(Ability, Roll_Type_Final) %>%
                          mutate(Counter = row_number(Ability))

# Pivoting Wider, Replacing NA's, sorting columns to standard DND 5e order
Skill_Ability_Final <- Skill_Ability_Sorted %>% 
                        pivot_wider(names_from = Ability, values_from = Roll_Type_Final) %>% 
                        mutate_all(~replace((.), is.na(.), "--")) %>%
                        select(Counter, Strength, Dexterity, Constitution, 
                               Intelligence, Wisdom, Charisma, Other) %>%
                        rbind(c("Total Rolls",735,2792,591,1085,1871,500,5935)) %>% print()
```

```
## # A tibble: 34 × 8
##    Counter Strength    Dexterity Constitution Intelligence Wisdom Charisma Other
##    <chr>   <chr>       <chr>     <chr>        <chr>        <chr>  <chr>    <chr>
##  1 1       Athletics   Acrobati… Concentrati… Alchemy      Anima… Charisma Atta…
##  2 2       Strength    Blacksmi… Constitution Arcana       Insig… Charism… Beard
##  3 3       Strength S… Dexterity Constitutio… History      Medic… Decepti… Coun…
##  4 4       --          Dexterit… --           Intelligence Perce… Disappo… Cutt…
##  5 5       --          Disguise… --           Intelligenc… Survi… Fart.    Dama…
##  6 6       --          Initiati… --           Investigati… Track… Intimid… Deat…
##  7 7       --          Sleight … --           Nature       Wisdom Musical… Dete…
##  8 8       --          Stealth   --           Religion     Wisdo… Perform… Dete…
##  9 9       --          Thieves'… --           --           --     Persuas… Divi…
## 10 10      --          Tinkering --           --           --     --       Fix  
## # ℹ 24 more rows
```

``` r
knitr::kable(Skill_Ability_Final, align = "c") %>% 
          kable_styling(full_width = T, font_size = 12) %>%
          row_spec(seq(from=1, to=34, by=2), background = "#eff1f2") %>%
          row_spec(34, font_size = 14, italic = T) %>%
          column_spec(1, bold=T, italic=T) %>%
          add_header_above(c("Index"=1, "Ability"=7),
                           font_size = 14) %>%
          add_header_above(c("Skills Organized by Associated Abilities"=8), 
                           font_size = 16, color = "white", background = "#000000")
```

<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(0, 0, 0, 255) !important;font-size: 16px;" colspan="8"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Skills Organized by Associated Abilities</div></th></tr>
<tr>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="1"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Index</div></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="7"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Ability</div></th>
</tr>
  <tr>
   <th style="text-align:center;"> Counter </th>
   <th style="text-align:center;"> Strength </th>
   <th style="text-align:center;"> Dexterity </th>
   <th style="text-align:center;"> Constitution </th>
   <th style="text-align:center;"> Intelligence </th>
   <th style="text-align:center;"> Wisdom </th>
   <th style="text-align:center;"> Charisma </th>
   <th style="text-align:center;"> Other </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Athletics </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Acrobatics </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Concentration </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Alchemy </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Animal Handling </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Charisma </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Attack </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> Strength </td>
   <td style="text-align:center;"> Blacksmith Tools </td>
   <td style="text-align:center;"> Constitution </td>
   <td style="text-align:center;"> Arcana </td>
   <td style="text-align:center;"> Insight </td>
   <td style="text-align:center;"> Charisma Save </td>
   <td style="text-align:center;"> Beard </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Strength Save </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Dexterity </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Constitution Save </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> History </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Medicine </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Deception </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Counterspell </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Dexterity Save </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Intelligence </td>
   <td style="text-align:center;"> Perception </td>
   <td style="text-align:center;"> Disappointment </td>
   <td style="text-align:center;"> Cutting Words </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Disguise Kit </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Intelligence Save </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Survival </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Fart. </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Damage </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Initiative </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Investigation </td>
   <td style="text-align:center;"> Tracking </td>
   <td style="text-align:center;"> Intimidation </td>
   <td style="text-align:center;"> Death Save </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Sleight of Hand </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Nature </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Wisdom </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Musical Taste </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Determine Effect </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 8 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Stealth </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Religion </td>
   <td style="text-align:center;"> Wisdom Save </td>
   <td style="text-align:center;"> Performance </td>
   <td style="text-align:center;"> Determine Focus </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 9 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Thieves' Tools </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Persuasion </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Divine Intervention </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 10 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Tinkering </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Fix </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Gambit of Ord </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 12 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Healing </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 13 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Heroes' Feast </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 14 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Inspiration </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 15 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Missile Snare </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 16 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> No reason. </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 17 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Other </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 18 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Panic </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 19 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Parry </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 20 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Percentile </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 21 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Potion Duration </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 22 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Recharge </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 23 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Resurrection Roll </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 24 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Second Wind </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 25 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Skill </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 26 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Sleep Arrow </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 27 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Spell Attack </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 28 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Spell Effect </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 29 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Spellcasting </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 30 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Telekinesis </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 31 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Test Roll </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 32 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> Trajectory </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 33 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Unknown </td>
  </tr>
  <tr>
   <td style="text-align:center;font-style: italic;font-size: 14px;font-weight: bold;font-style: italic;"> Total Rolls </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 735 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 2792 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 591 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 1085 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 1871 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 500 </td>
   <td style="text-align:center;font-style: italic;font-size: 14px;"> 5935 </td>
  </tr>
</tbody>
</table>

&emsp; Note: Both "Thieves' Tools" and "Tinkering" were sometimes treated as Dexterity and sometimes treated as Intelligence. In what I could find, both seemed to be predominately treated as Dexterity in this campaign, so it's what I went with. Attack rolls were placed in the "Other" column because while the appropriate ability score would be known, that information was not included in the data set. 688 of the 2,792 Dexterity rolls were Initiative, meaning 24.6% of the Dexterity rolls were *getting into* combat. Of the 5,935 "Other" rolls, there were 3,147 "Attack" rolls and 2,161 "Damage rolls. That means at least 89.4% of the "Other" rolls were *in* combat. 

<div style = "float:left; position:relative; width:49.7%; left: 5px; top: 0px;">
<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(114, 165, 206, 255) !important;font-size: 16px;" colspan="3"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Percent of Total Rolls by Ability</div></th></tr>
  <tr>
   <th style="text-align:center;"> Ability </th>
   <th style="text-align:center;"> Rolls </th>
   <th style="text-align:center;"> % of Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Strength </td>
   <td style="text-align:center;"> 735 </td>
   <td style="text-align:center;"> 5.4 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Dexterity </td>
   <td style="text-align:center;"> 2792 </td>
   <td style="text-align:center;"> 20.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Constitution </td>
   <td style="text-align:center;"> 591 </td>
   <td style="text-align:center;"> 4.4 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Intelligence </td>
   <td style="text-align:center;"> 1085 </td>
   <td style="text-align:center;"> 8.0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Wisdom </td>
   <td style="text-align:center;"> 1871 </td>
   <td style="text-align:center;"> 13.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Charisma </td>
   <td style="text-align:center;"> 500 </td>
   <td style="text-align:center;"> 3.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Other </td>
   <td style="text-align:center;"> 5935 </td>
   <td style="text-align:center;"> 43.9 </td>
  </tr>
</tbody>
</table>
</div>

<div style = "float:right; position:relative; width:49.7%; left: 5px; top: 0px;">
<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(149, 133, 92, 255) !important;font-size: 16px;" colspan="3"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Percent of Total Rolls by Ability (Without Other)</div></th></tr>
  <tr>
   <th style="text-align:center;"> Ability </th>
   <th style="text-align:center;"> Rolls </th>
   <th style="text-align:center;"> % of Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Strength </td>
   <td style="text-align:center;"> 735 </td>
   <td style="text-align:center;"> 9.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Dexterity </td>
   <td style="text-align:center;"> 2792 </td>
   <td style="text-align:center;"> 36.9 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Constitution </td>
   <td style="text-align:center;"> 591 </td>
   <td style="text-align:center;"> 7.8 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Intelligence </td>
   <td style="text-align:center;"> 1085 </td>
   <td style="text-align:center;"> 14.3 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Wisdom </td>
   <td style="text-align:center;"> 1871 </td>
   <td style="text-align:center;"> 24.7 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Charisma </td>
   <td style="text-align:center;"> 500 </td>
   <td style="text-align:center;"> 6.6 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;font-weight: bold;font-style: italic;"> NA </td>
   <td style="text-align:center;color: white !important;"> 1 </td>
   <td style="text-align:center;color: white !important;"> 1 </td>
  </tr>
</tbody>
</table>

</div>

&emsp; Examining the demands of the story based on the rolls, it pays to be Dexterous and Wise in Campaign 1. Many of Campaign 2's characters would have done very well against the obstacles Vox Machina faced just based on the distribution of their ability scores.

---

# 5. Success In The Face Of The The Nearly Impossible 

&emsp; Now that some context has been added, it's time to zoom in on the rolls of greatest interest, the one's that exceeded the highest tier of difficulty class.

### 5.1. Pulling out only those rolls

&emsp; First any roll that had no associated character needed to be removed. Next I filtered out rolls that were known to or suspected to not have been done with a d20. Damage has an incredibly high ceiling, so achieving over 30 does not get the same kind of reaction as passing a Difficulty Check with over 30, so while it will be incorporated into a later examination, for now it had to go. If there was no roll type it would have been impossible to determine what the roll was for, so those were removed. Lastly, the main focus, only rolls that totaled (roll on the dice and any modifiers) were kept. 


``` r
# DC Greater or equal to 30
DC30_Rolls_wStealth <- VM_Campaign %>% 
                        filter(!is.na(Character_Final)) %>%                    
    
                        filter(Roll_Type_Final != "Beard") %>%
                        filter(Roll_Type_Final != "d100") %>%                      
                        filter(Roll_Type_Final != "Damage") %>% 
                        filter(Roll_Type_Final != "Determine Effect") %>%
                        filter(Roll_Type_Final != "Divine Intervention") %>%
                        filter(Roll_Type_Final != "Healing") %>%
                        filter(Roll_Type_Final != "Percentile") %>%
  
                        filter(!is.na(Roll_Type_Final)) %>%
  
                        filter(Total_Final >= 30)
```


``` r
DC30_Rolls_wStealth %>% nrow() # 590
```

&emsp; I debated keeping Stealth rolls. Because of the well-loved spell [Pass Without a Trace](https://www.dndbeyond.com/spells/2201-pass-without-trace) it is possible to get absurdly high rolls on Stealth checks. However, because the cast and other players still have that "wow" reaction when a high roll is made even the extra magical help, I kept it in.

&emsp; Before filtering there were 13,514 rolls recorded in Campaign 1. After filtering all except the total, there were 11,001 rolls (81.4% of the total) still remaining. When the filter for the roll total was added, that number dropped to 590. Only 4.4% of the rolls in Campaign 1 (pre-filtering) were 30 or above. These are truly the cream of the crop, but honestly more frequent than I expected.

### 5.2. Who Performed These Feats?

&emsp; The first thing people like to know when you tell them about a particularly notable roll is who rolled that high? That's what I looked at first. 


``` r
# DC 30+ Table by Character
DC30_Character <- DC30_Rolls_wStealth %>% 
                    group_by(Character_Final) %>%
                    count(Total_Final) %>%
                    pivot_wider(names_from = Character_Final, values_from = n) %>%
                    mutate_all(~replace((.), is.na(.), "--")) %>%
                    select(Total_Final,'Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan","Vex'ahlia",
                         'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra") %>%
                    arrange(Total_Final)

knitr::kable(DC30_Character, align = "c",
                col.names = c("Total", 'Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan","Vex'ahlia",
                             'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra")) %>% 
          kable_styling(full_width = T, font_size = 12) %>%
          row_spec(seq(from=1, to=18, by=2), background = "#eff1f2") %>%
          pack_rows(index = c("30+ Club"=5,"35+ Club"=5,"40+ Club"=5,"45+ Club"=3)) %>%
          column_spec(1, bold=T, italic=T) %>%
          add_header_above(c(" "=1, "Main Party"=7, "Guests/Inactive Members"=6),
                           font_size = 14) %>%
          add_header_above(c("Characters Who Rolled 30+"=14), 
                           font_size = 16, color = "white", background = "#352b41")
```

<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(53, 43, 65, 255) !important;font-size: 16px;" colspan="14"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Characters Who Rolled 30+</div></th></tr>
<tr>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="1"></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="7"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Main Party</div></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="6"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Guests/Inactive Members</div></th>
</tr>
  <tr>
   <th style="text-align:center;"> Total </th>
   <th style="text-align:center;"> Grog </th>
   <th style="text-align:center;"> Keyleth </th>
   <th style="text-align:center;"> Percy </th>
   <th style="text-align:center;"> Pike </th>
   <th style="text-align:center;"> Scanlan </th>
   <th style="text-align:center;"> Vax'ildan </th>
   <th style="text-align:center;"> Vex'ahlia </th>
   <th style="text-align:center;"> Arkhan </th>
   <th style="text-align:center;"> Lyra </th>
   <th style="text-align:center;"> Tiberius </th>
   <th style="text-align:center;"> Tova </th>
   <th style="text-align:center;"> Trinket </th>
   <th style="text-align:center;"> Zahra </th>
  </tr>
 </thead>
<tbody>
  <tr grouplength="5"><td colspan="14" style="border-bottom: 1px solid;"><strong>30+ Club</strong></td></tr>
<tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 30 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 15 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 12 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 29 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 15 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 50 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 43 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 31 </td>
   <td style="text-align:center;"> 18 </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 22 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 23 </td>
   <td style="text-align:center;"> 27 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 32 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 14 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 10 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 29 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 21 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 33 </td>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 20 </td>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 34 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr grouplength="5"><td colspan="14" style="border-bottom: 1px solid;"><strong>35+ Club</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 35 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 13 </td>
   <td style="text-align:center;"> 11 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 36 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 37 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 15 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 38 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 39 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 9 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr grouplength="5"><td colspan="14" style="border-bottom: 1px solid;"><strong>40+ Club</strong></td></tr>
<tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 40 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 41 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 42 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 43 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 44 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr grouplength="3"><td colspan="14" style="border-bottom: 1px solid;"><strong>45+ Club</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 45 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 46 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> -- </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 47 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
   <td style="text-align:center;"> -- </td>
  </tr>
</tbody>
</table>


``` r
Outrageous_Mini <- DC30_Rolls_wStealth %>% filter(Total_Final >= 45) %>% select(Character_Final, Roll_Type_Final, Total_Final) %>%
               knitr::kable(align = "c",
               col.names = c("Character", "Roll Type", "Total")) %>% 
               kable_styling(full_width = F) %>%
               row_spec(1, background = "#a1b556", color = "white") %>%
               row_spec(c(2,7:8), background = "#3b6e89",color = "white") %>%
               row_spec(c(3:6), background = "#352b41",color = "white") %>%
               add_header_above(c("The Truly Outrageous Rolls: 45 and Over" =3), font_size = 16)
```

<div style = "float:right; position:relative; width:40%; left: 5px; top: 0px;">

``` r
Outrageous_Mini
```

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 16px;" colspan="3"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">The Truly Outrageous Rolls: 45 and Over</div></th></tr>
  <tr>
   <th style="text-align:center;"> Character </th>
   <th style="text-align:center;"> Roll Type </th>
   <th style="text-align:center;"> Total </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(161, 181, 86, 255) !important;"> Keyleth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(161, 181, 86, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(161, 181, 86, 255) !important;"> 47 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Vex'ahlia </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> 46 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Vax'ildan </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> 45 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Vax'ildan </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> 46 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Vax'ildan </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> 45 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Vax'ildan </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(53, 43, 65, 255) !important;"> 45 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Vex'ahlia </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> 46 </td>
  </tr>
  <tr>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Vax'ildan </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> Stealth </td>
   <td style="text-align:center;color: white !important;background-color: rgba(59, 110, 137, 255) !important;"> 46 </td>
  </tr>
</tbody>
</table>
</div>

&emsp; Here's a closer examination of the atmospherically high rolls. As expected, they're all for Stealth and were likely magically assisted. Pass Without a Trace adds a +10 modifier to Stealth rolls.

---

### 5.3. What Were These Feats?

&emsp; Next people ask what was happening when they rolled that high. 


``` r
# What were the impossible rolls?
DC30_Type <- DC30_Rolls_wStealth %>% 
              group_by(Character_Final) %>%
              count(Roll_Type_Final) %>%
              pivot_wider(names_from = Character_Final, values_from = n) %>%
              replace_na(list('Arkhan'=0,'Grog'=0,'Keyleth'=0,'Lyra'=0,'Percy'=0,'Pike'=0,'Scanlan'=0,
                              'Taryon'=0,'Tiberius'=0,'Tova'=0,"Trinket"=0,"Vax'ildan"=0,"Vex'ahlia"=0,"Zahra"=0)) %>%
              select(Roll_Type_Final,'Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan","Vex'ahlia",
                         'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra") %>%
              arrange(Roll_Type_Final) %>%
              bind_rows(summarise_all(., ~if(is.numeric(.)) sum(.) else "Total"))

knitr::kable(DC30_Type, align = "c",
             col.names = c("Roll Type", 'Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan","Vex'ahlia",
                         'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra")) %>% 
          kable_styling(full_width = T, font_size = 12) %>%
          row_spec(seq(from=1, to=23, by=2), background = "#eff1f2") %>%
          row_spec(23, font_size = 14, italic = T) %>%
          column_spec(1, bold=T, italic=T) %>%
          add_header_above(c(" "=1, "Main Party"=7, "Guests / Inactive Members"=6),
                           font_size = 14) %>%
          add_header_above(c("The Skill Types of the 30+ Rolls"=14), 
                           font_size = 16, color = "white", background = "#7f2820")
```

<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(127, 40, 32, 255) !important;font-size: 16px;" colspan="14"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">The Skill Types of the 30+ Rolls</div></th></tr>
<tr>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="1"></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="7"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Main Party</div></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="6"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Guests / Inactive Members</div></th>
</tr>
  <tr>
   <th style="text-align:center;"> Roll Type </th>
   <th style="text-align:center;"> Grog </th>
   <th style="text-align:center;"> Keyleth </th>
   <th style="text-align:center;"> Percy </th>
   <th style="text-align:center;"> Pike </th>
   <th style="text-align:center;"> Scanlan </th>
   <th style="text-align:center;"> Vax'ildan </th>
   <th style="text-align:center;"> Vex'ahlia </th>
   <th style="text-align:center;"> Arkhan </th>
   <th style="text-align:center;"> Lyra </th>
   <th style="text-align:center;"> Tiberius </th>
   <th style="text-align:center;"> Tova </th>
   <th style="text-align:center;"> Trinket </th>
   <th style="text-align:center;"> Zahra </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Acrobatics </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 15 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Arcana </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Athletics </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Attack </td>
   <td style="text-align:center;"> 51 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 57 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 45 </td>
   <td style="text-align:center;"> 43 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Charisma Save </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Constitution Save </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Deception </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 13 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Dexterity Save </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Initiative </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Intelligence </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Investigation </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Nature </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Perception </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 16 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 36 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Performance </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Persuasion </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Stealth </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 24 </td>
   <td style="text-align:center;"> 25 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 99 </td>
   <td style="text-align:center;"> 55 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Strength </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Survival </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Thieves' Tools </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Tinkering </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> Unknown </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> Wisdom Save </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;font-weight: bold;font-style: italic;"> Total </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 60 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 40 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 90 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 39 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 192 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 149 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-style: italic;font-size: 14px;"> 1 </td>
  </tr>
</tbody>
</table>

### 5.4. When Did They Happen?

&emsp; Finally, people ask when they happened. 


``` r
# When were these impossible rolls?
DC30_Timeline <- DC30_Rolls_wStealth %>% 
                  group_by(Episode_Final) %>%                      
                  count(Character_Final) %>%
                  pivot_wider(names_from = Character_Final, values_from = n) %>%
                  replace_na(list('Arkhan'=0,'Grog'=0,'Keyleth'=0,'Lyra'=0,'Percy'=0,'Pike'=0,
                                  'Scanlan'=0,'Taryon'=0,'Tiberius'=0,'Tova'=0,"Trinket"=0,
                                  "Vax'ildan"=0,"Vex'ahlia"=0,"Zahra"=0)) %>%
                  select('Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan",
                         "Vex'ahlia",'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra")
      
DC30_Timeline_Final <- as.data.frame(DC30_Timeline) %>% 
                        mutate("Total" = rowSums(DC30_Timeline[sapply(DC30_Timeline, is.integer)]), 
                               .after = "Vex'ahlia")
```


``` r
Top30_Episodes<- table(DC30_Rolls_wStealth$Episode_Final) %>% as.data.frame() %>% arrange(desc(Freq))
names(Top30_Episodes)[1] <- "Episode"

Top30_Final <- Top30_Episodes[1:10,] %>% 
                mutate(Arc = c("Vecna","Vecna","Vecna","Taryon Darrington",
                              "Taryon Darrington","Taryon Darrington","The Chroma Conclave",
                              "Vecna","The Chroma Conclave", "The Chroma Conclave"), 
                       .after = Episode)
```


``` r
Top30_Mini <- knitr::kable(Top30_Final, align = "c", 
                           col.names = c("Episode", "Arc", "Number of Rolls 30 and Over")) %>% 
                    kable_styling(full_width = F) %>%
                    row_spec(seq(from=1,to=10,by=2), background = "#eff1f2") %>%
                    add_header_above(c("Episodes with the Most Rolls 30 and Over" =3), font_size = 16)
```

--- 

<div style = "float:right; position:relative; width:50%; left: 10px; top: 0px;">

``` r
Top30_Mini
```

<table class="table" style="width: auto !important; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 16px;" colspan="3"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Episodes with the Most Rolls 30 and Over</div></th></tr>
  <tr>
   <th style="text-align:center;"> Episode </th>
   <th style="text-align:center;"> Arc </th>
   <th style="text-align:center;"> Number of Rolls 30 and Over </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 113 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Vecna </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 33 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 114 </td>
   <td style="text-align:center;"> Vecna </td>
   <td style="text-align:center;"> 24 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 108 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Vecna </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 23 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 92 </td>
   <td style="text-align:center;"> Taryon Darrington </td>
   <td style="text-align:center;"> 21 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 88 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> Taryon Darrington </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 19 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 93 </td>
   <td style="text-align:center;"> Taryon Darrington </td>
   <td style="text-align:center;"> 17 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 44 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> The Chroma Conclave </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 112 </td>
   <td style="text-align:center;"> Vecna </td>
   <td style="text-align:center;"> 16 </td>
  </tr>
  <tr>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 68 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> The Chroma Conclave </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 15 </td>
  </tr>
  <tr>
   <td style="text-align:center;"> 47 </td>
   <td style="text-align:center;"> The Chroma Conclave </td>
   <td style="text-align:center;"> 14 </td>
  </tr>
</tbody>
</table>
</div>

&emsp; It makes sense that so many of these episodes with the very highest count of rolls 30 and over were in the later story arcs. Having leveled up so much, the modifiers that are getting added to their rolls helped push the totals they roll higher and higher, reflecting their growth throughout their story.   

&emsp; Here's a full breakdown of when all of the 30+ rolls occurred including their episodes and arcs:

---


``` r
knitr::kable(DC30_Timeline_Final, align = "c",
             col.names = c("Episode", 'Grog','Keyleth','Percy','Pike','Scanlan',"Vax'ildan","Vex'ahlia",
                         "Total",'Arkhan','Lyra','Tiberius','Tova',"Trinket","Zahra")) %>% 
          kable_styling(full_width = T, font_size = 12) %>%
          pack_rows(index = c("Arc 1: Kraghammer and Vasselheim (49)" = 19,
                              "Arc 2: The Briarwoods (39)" = 15,
                              "Arc 3: The Chroma Conclave (236)" = 43,
                              "Arc 4: Taryon Darrington (85)" = 14,
                              "Arc 5: Vecna (172)" = 15)) %>%
          row_spec(seq(from=1,to=105,by=2), background = "#eff1f2") %>%
          column_spec(c(1,9), bold=T, italic=T) %>%
          add_header_above(c(" "=1, "Main Party"=7, " "=1, "Guests/Inactive Members"=6),
                           font_size = 14) %>%
          add_header_above(c("Timeline of 30+ Rolls - Arcs Included"=15), 
                           font_size = 16, color = "white", background = "#762e64")
```

<table class="table" style="font-size: 12px; margin-left: auto; margin-right: auto;">
 <thead>
<tr><th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; color: white !important;padding-right: 4px; padding-left: 4px; background-color: rgba(118, 46, 100, 255) !important;font-size: 16px;" colspan="15"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Timeline of 30+ Rolls - Arcs Included</div></th></tr>
<tr>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="1"></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="7"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Main Party</div></th>
<th style="empty-cells: hide;border-bottom:hidden;" colspan="1"></th>
<th style="border-bottom:hidden;padding-bottom:0; padding-left:3px;padding-right:3px;text-align: center; font-size: 14px;" colspan="6"><div style="border-bottom: 1px solid #ddd; padding-bottom: 5px; ">Guests/Inactive Members</div></th>
</tr>
  <tr>
   <th style="text-align:center;"> Episode </th>
   <th style="text-align:center;"> Grog </th>
   <th style="text-align:center;"> Keyleth </th>
   <th style="text-align:center;"> Percy </th>
   <th style="text-align:center;"> Pike </th>
   <th style="text-align:center;"> Scanlan </th>
   <th style="text-align:center;"> Vax'ildan </th>
   <th style="text-align:center;"> Vex'ahlia </th>
   <th style="text-align:center;"> Total </th>
   <th style="text-align:center;"> Arkhan </th>
   <th style="text-align:center;"> Lyra </th>
   <th style="text-align:center;"> Tiberius </th>
   <th style="text-align:center;"> Tova </th>
   <th style="text-align:center;"> Trinket </th>
   <th style="text-align:center;"> Zahra </th>
  </tr>
 </thead>
<tbody>
  <tr grouplength="19"><td colspan="15" style="border-bottom: 1px solid;"><strong>Arc 1: Kraghammer and Vasselheim (49)</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 1.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 2.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 3.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 4.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 5.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 6.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 7.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 8.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 10.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 11.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 13.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 15.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 16.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 17.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 18.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 19.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 20.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 21.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 22.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr grouplength="15"><td colspan="15" style="border-bottom: 1px solid;"><strong>Arc 2: The Briarwoods (39)</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 24.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 25.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 26.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 28.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 29.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 10 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 30.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 31.1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 31.2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 32.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 33.2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 34.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 35.2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 36.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 37.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 38.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr grouplength="43"><td colspan="15" style="border-bottom: 1px solid;"><strong>Arc 3: The Chroma Conclave (236)</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 39.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 40.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 41.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 42.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 13 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 43.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 44.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 7 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 16 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 45.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 46.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 12 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 47.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 14 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 48.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 49.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 9 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 50.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 9 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 51.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 10 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 52.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 53.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 54.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 55.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 56.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 57.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 58.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 59.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 60.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 61.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 62.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 63.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 64.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 65.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 66.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 67.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 68.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 8 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 15 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 69.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 70.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 71.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 72.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 75.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 76.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 77.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 78.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 79.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 80.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 81.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 82.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 10 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 83.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 10 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr grouplength="14"><td colspan="15" style="border-bottom: 1px solid;"><strong>Arc 4: Taryon Darrington (85)</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 84.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 85.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 87.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 88.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 19 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 90.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 91.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 92.0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 21 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 93.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 6 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 17 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 94.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 95.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 96.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 97.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 98.0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 8 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 99.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr grouplength="15"><td colspan="15" style="border-bottom: 1px solid;"><strong>Arc 5: Vecna (172)</strong></td></tr>
<tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 100.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 11 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 101.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 102.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 8 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 104.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 105.0 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 9 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 106.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 107.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 108.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 10 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 23 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 109.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 110.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 8 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 11 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 111.0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 3 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 14 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 112.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 7 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 16 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 113.0 </td>
   <td style="text-align:center;"> 4 </td>
   <td style="text-align:center;"> 2 </td>
   <td style="text-align:center;"> 6 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 10 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 33 </td>
   <td style="text-align:center;"> 5 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;" indentlevel="1"> 114.0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 9 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 4 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 1 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 5 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 3 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;font-weight: bold;font-style: italic;"> 24 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 2 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
   <td style="text-align:center;background-color: rgba(239, 241, 242, 255) !important;"> 0 </td>
  </tr>
  <tr>
   <td style="text-align:center;padding-left: 2em;font-weight: bold;font-style: italic;" indentlevel="1"> 115.0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;"> 1 </td>
   <td style="text-align:center;font-weight: bold;font-style: italic;"> 2 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
   <td style="text-align:center;"> 0 </td>
  </tr>
</tbody>
</table>

---

# 6. Conclusion and Future Examination

&emsp; In the face of great adversity, success feels especially good. To not only succeed, but at the same time demonstrate great ability through skill or luck or some combination of the two, creates a moment that people talk about for a long time -  whether it happened in a tabletop game or out the sporting field. High rolls are often akin this kind of triumph, and that's why the elicit such reactions. With the timeline of rolls over 30, fans can revisit those episodes where doing the impossible was the most frequent.

&emsp; Knowing when the highest rolls of the campaign occurred is fascinating, but what about before all the modifiers? Who has a tendency of rolling high on the dice themselves? Does Taliesen Jaffe really have a penchant for Natural 20's? And if so, how much higher than the statistical average does he roll them? These will be some of the areas explored in the next examination of this data set.


---
title: Learning Neovim (pt. 2)
author: Zach Hedeen
date: '2024-08-29'
slug: learning-neovim-pt-2
categories:
  - Neovim
tags:
  - Notes
---


# Version Troubles

&emsp; I've been playing around with Neo Vim a lot more than I've been writing about it. It's been 19 days since I first got trapped and despite that short time, I feel quite comfortable using the tool. There is certainly a ton of learning still to go before I'll be able to zoom around and manipulate code at the speed of thought, but progress is progress. 

&emsp; The version that the Windows Subsystem for Linux installs is v0.6.1. This version is too old to support a lot of the plug-ins and additional tools that make Neo Vim especially powerful. Too much time was spent wondering why the tutorials I tried to follow online weren't working only for the answer to be that simple. If things aren't working for you, make sure you're using a new enough version of Neo Vim. 

# :Tutor

&emsp; To open the Tutorial, enter the command `:Tutor`. While this post will summarize the main points of the page's many lessons, nothing is going to replace actually practicing with the tools. Make sure to do the tutorial yourself and find as many opportunities as you can to employ and expand upon the skills you learn. 

&emsp; *Everything from here on is a direct copy of the 'Welcome to the VIM Tutor' page. Credit to the authors Bram Moolenaar and Felipe Morales.*

# Lesson 1 Summary

1. The cursor is moved using either the arrow keys or the hjkl keys.  
&emsp; `h (left) - j (down) - k (up) - l (right)`  

2. To start Vim from the shell prompt type:  
&emsp; `$ nvim FILENAME`  

3. To exit Vim type: <Esc> :q! <Enter> to trash all changes.  
&emsp; `OR type: <Esc> :wq <Enter> to save the changes.`  

4. To delete the character at the cursor type: x  

5. To insert or append text type:  
&emsp; `i insert text <Esc> &emsp; insert before the cursor.`  
&emsp; `A append text <Esc> &emsp; append after the line.`  

NOTE: Pressing <Esc> will place you in Normal mode or will cancel an unwanted and partially completed command.
  
# Lesson 2 Summary 

1. To delete from the cursor up to the next word type:    dw  
2. To delete from the cursor to the end of a line type:   d$  
3. To delete a whole line type:                           dd  
4. To repeat a motion prepend it with a number:           2w  

5. The format for a change command is:

&emsp; `operator  [number]  motion`

where:  
&emsp; operator - is what to do, such as d for delete  
&emsp; [number] - is an optional count to repeat the motion  
&emsp; motion   - moves over the text to operate on, such as:  
&emsp; &emsp; `w` (word),  
&emsp; &emsp; `$` (to the end of line), etc.

6. To move to the start of the line use a zero: 0

7. To undo previous actions, type:            `u`  (lowercase u)  
   To undo all the changes on a line, type:   `U`  (capital U)  
   To undo the undo's, type:                  `<C-r>`  

# Lesson 3 Summary

1. To put back text that has just been deleted, type `p`. This puts the 434 deleted text AFTER the cursor 
(if a line was deleted it will go on 435 line below the cursor).  
2. To replace the character under the cursor, type `r` and then the character you want to have there.  
3. The change operator allows you to change from the cursor to where the motion takes you. Type `ce` to change from the cursor to the end of the word, `c$` to change to the end of a line.  

4. The format for change is:  
&emsp; c   [number]   motion  

# Lesson 4 Summary 

1. `<C-g>` - displays your location and the file status.  
   `G` - moves to the end of the file.  
   `number G` - moves to that line number.  
   `gg` - moves to the first line.  

2. Typing `/` followed by a phrase searches FORWARD for the phrase.  
   Typing `?` followed by a phrase searches BACKWARD for the phrase.  
   After a search type `n` to find the next occurrence in the same direction or `N` to search in the opposite direction.  
   `<C-o>` - takes you back to older positions,  
   `<C-i>` to newer positions.  

3. Typing `%` while the cursor is on a (,),[,],{, or } goes to its match.  

4. To substitute new for the first old in a line type  
&emsp; `:s/old/new`  

To substitute new for all 'old's on a line type  
&emsp; `:s/old/new/g`  

To substitute phrases between two line #'s type  
&emsp; `:#,#s/old/new/g`  

To substitute all occurrences in the file type  
&emsp; `:%s/old/new/g`  
  
To ask for confirmation each time add 'c'  
&emsp; `:%s/old/new/gc`  
  
# Lesson 5 Summary 

1. `:!` - command executes an external command.  
&emsp; Some useful examples are:  
&emsp; &emsp; `:!ls` - shows a directory listing  
&emsp; &emsp; `:!rm FILENAME` - removes file FILENAME  
 
2. `:w FILENAME` - writes the current Vim file to disk with name FILENAME.  

3. `v motion :w FILENAME` - saves the Visually selected lines in file FILENAME.  

4. `:r FILENAME` - retrieves disk file FILENAME and puts it below the cursor position.  

5. `:r !dir` - reads the output of the dir command and puts it below the cursor position.  
  
# Lesson 6 Summary

1. Type `o` to open a line BELOW the cursor and start Insert mode.  
   Type `O` to open a line ABOVE the cursor.  

2. Type `a` to insert text AFTER the cursor.  
   Type `A` to insert text after the end of the line.  

3. The `e` command moves to the end of a word.  

4. The `y` operator copies text, `p` pastes it.  

5. Typing a capital `R` enters Replace mode until `<Esc>` is pressed.  

6. Typing `:set xxx` sets the option "xxx". Some options are:  
&emsp; 'ic' 'ignorecase' - ignore upper/lower case when searching  
&emsp; 'is' 'incsearch' - show partial matches for a search phrase  
&emsp; 'hls' 'hlsearch' - highlight all matching phrases  

You can either use the long or the short option name.  
 
7. Prepend "no" to switch an option off:  
&emsp; `:set noic`  

8. Prepend "inv" to toggle an option:  
&emsp; `:set invic`  
  
# Lesson 7 Summary

1. Type `:help` or press `<F1>` or `<Help>` to open a help window.  

2. Type `:help` TOPIC to find help on TOPIC.  

3. Type `<C-w><C-w>` to jump to another window  

4. Type `:q` to close the help window  

5. Create a vimrc startup script to keep your preferred settings.  

6. While in command mode, press `<C-d>` to see possible completions. Press `<Tab>` to use one completion.  
  
# Conclusion and Online Resources

This was intended to give a brief overview of the Vim editor, just enough to allow you to use the editor fairly easily. It is far from complete as Vim has many many more commands. Consult the help often.There are many resources online to learn more about vim. Here's a bunch of them:  

- [Learn Vim Progressively](http://yannesposito.com/Scratch/en/blog/Learn-Vim-Progressively/)
- [Learning Vim in 2013](http://benmccormick.org/learning-vim-in-2014/)
- [Vimcasts](http://vimcasts.org/)
- [Vim Video-Tutorials by Derek Wyatt](http://derekwyatt.org/vim/tutorials/)
- [Learn Vimscript the Hard Way](http://learnvimscriptthehardway.stevelosh.com/)
- [7 Habits of Effective Text Editing](http://www.moolenaar.net/habits.html)
- [vim-galore](https://github.com/mhinz/vim-galore)

If you prefer a book, Practical Vim by Drew Neil is recommended often (the sequel, Modern Vim, includes material specific to nvim).  

This tutorial was written by Michael C. Pierce and Robert K. Ware, Colorado School of Mines using ideas supplied by Charles Smith, Colorado State University. E-mail: bware@mines.colorado.edu.  

Modified for Vim by Bram Moolenaar.  
Modified for vim-tutor-mode by Felipe Morales.  

# Additional Commands and Thoughts

`b` - go back one word  
`H` - jump to the top visible line  
`L` - jump to the bottom visible line  
`gM` - jump to the middle of the line   
`<C-f>` - go forward one page  
`<C-b>` - go backward one page  
`:#,# %norm xxx` - apply a series of commands (xxx) to all lines in the specified range. Do not include the numbered lines if you want changes to happen to all lines in the document.  
`:split` - splits the screen horizontally with another document in Neo Vim  
`:vsplit` - splits the screen vertically with another document in Neo Vim  
`:new` - creates a new document with Neo Vim  
`:only` - closes all other screen splits  

&emsp; The basics covered in the tutorial have been incredibly helpful. The additional commands in this last section were ones that I found through reading the extended documentation. There are times I'm editing text or code in other IDEs and find myself wishing I had some of the capabilities that Neo Vim does. It sounds like there are extensions in most IDEs that allow the utilization of Vim motions so they can be enjoyed without having to give up all the things you like about your current setup. 

&emsp; I've found some series on YouTube that discuss how to get more out of Neo Vim. My notes on those videos will be the subject of my next posts about Neo Vim. 


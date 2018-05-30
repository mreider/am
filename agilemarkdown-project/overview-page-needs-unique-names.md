# Overview page needs unique names

Project: Agilemarkdown-project

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Project: Agilemarkdown-project  
Created: 2018-05-30 06:20 PM  
Modified: 2018-05-30 09:50 PM  

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-02 11:19 AM  
Modified: 2018-05-22 08:49 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 1  

## Problem statement

It looks like Gollum, the Github Wiki, does not support duplicate file names in different directories. So creating the file 0-overview.md is problematic. If you look at the overview files on the Wiki, they actually display the first overview page from the first directory. So we need to make sure that the overview files are unique. We should also, at some point, make sure all story names are unique, but let's not worry about that yet.

## Possible solution

- Instead of naming the file 0-overview.md, we could use a unique name based on the project / folder name.

- Perhaps a better idea, since the folder name could be super long, is to throw a unique 4 digit number on the end of the file. So instead of 0-overview, we could name it 0index-4565. Seems like a decent naming convention, and the word index is shorter than overview...

## Comments

 @falconandy it looks like you are still creating the 0-overview page, even though you have a new page.

Also, you are not updating `_Sidebar.md` with the links to these index pages.

Do you think it might be better to name the index pages according to the backlog name, and put them at the root level instead? Then these crazy '0-' names can go away.

 @mreider It seems you didn't rebuild the Go program. Is it right?   
Your suggestion about index page names is better than the current solution, I think. Let's try it! 

## Attachments

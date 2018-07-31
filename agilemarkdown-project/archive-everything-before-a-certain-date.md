# Archive everything before a certain date

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags:   
Status: finished  
Assigned: falconandy  
Estimate: 2  

## Problem statement

It is a pain to use change-status and archive stories one-by-one.

## Possible solution

Create a new command 'am archive' that takes a date (validate format) as yyyy-mm-dd and
adds the `archive:1` key / pair to every story before that date. If the story is already archived,
make sure not to add the key twice.

## Comments

 @mreider "before that date" Should I compare "create date" or "modified date"? "Before" - do you mean strict less (<) or <= ? 
 @falconandy let's use modified date and do <=

## Attachments

## Metadata

Created: 2018-05-17 09:21 PM  
Modified: 2018-05-23 08:30 PM  
Author: Matt Reider  

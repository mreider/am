# Archive everything before a certain date

[project](../agilemarkdown-project.md) [archive](archive.md) [index](../index.md) [ideas](../ideas.md) [tags](../tags.md)

Created: 2018-05-17 09:21 PM  
Modified: 2018-05-20 08:02 PM  
Tags:   
Author: Matt Reider  
Status: planned  
Assigned: falconandy  
Estimate: 2  

## Problem statement

It is a pain to use change-status and archive stories one-by-one.

## Possible solution

Create a new command 'am archive' that takes a date (validate format) as yyyy-mm-dd and
adds the `archive:1` key / pair to every story before that date. If the story is already archived,
make sure not to add the key twice.

## Comments


## Attachments

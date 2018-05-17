Title: archive everything before a certain date  
Created: 2018-05-17 09:21 PM  
Modified: 2018-05-17 09:21 PM  
Tags:   
Author: Matt Reider  
Status: planned  
Assigned: falconandy
Estimate: 2

# Archive everything before a certain date

## Problem statement

It is a pain to use change-status and archive stories one-by-one.

## Possible solution

Create a new command 'am archive' that takes a date (validate format) as yyyy-mm-dd and
adds the `archive:1` key / pair to every story before that date. If the story is already archived,
make sure not to add the key twice.

## Comments

@falconandy another new bit for you

## Attachments

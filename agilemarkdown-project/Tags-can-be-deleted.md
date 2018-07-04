# Tags can be deleted

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Created: 2018-07-04 03:22 PM  
Modified: 2018-07-04 03:27 PM  
Tags: Cleanup  
Author: Matt Reider  
Status: planned 
Assigned: falconandy  
Estimate: 2  

## Problem statement

There are a lot of things to cleanup if you delete a tag. This should be done more easily.

## Possible solution

A new command:

‘’’
am delete-tag [tag]
This will delete links to ideas and timelines ok?(y or n):y

Tag deleted. Sync to regenerate files.
‘’’

If answer is yes then delete this tag from every story across all projects.

Also delete the forecasted dates for that tag across all stories.

## Comments

## Attachments


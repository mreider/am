# Tags can have timelines

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Created: 2018-07-04 01:21 PM  
Modified: 2018-07-04 02:12 PM  
Tags:   
Author: Matt Reider  
Status: unplanned  
Assigned: falconandy  
Estimate: 5  

## Problem statement

People want to see a gantt view of certain stories that relate to one another in a gantt chart

## Possible solution

We could use tags and a new command to build a timeline of stories.

This command:

‘am timeline [tag]’

First the command will ask for the sequence of stories so you can add dates:

‘’’
A some story
B some other story
C another story
D more stories

Enter the story order:
A,b,D,C

Enter dates as YYYY-MM-DD

some story
Start date: 2018-05-10
End date: 2018-05-12

some other story
Start date: 2018-05-13
End date: 2018-05-20

More stories
Start date: 2018-05-21
End date: 2018-05-22

Another story
Start date: 2018-05-23
End date: 2018-05-24

Timeline set
Gantt generated for [tag]
‘’’

You can use https://github.com/gerald1248/timeline

Please do validation on dates and repeat question if date is wrong with error message.

Also validate story list. Not every story needs to be in the list, but don’t allow a letter that isn’t valid.

So A,B is valid (can miss others)
But A,Z is invalid

I think we need different forecast dates per tag. I will create another story for that.

Gantt charts should be listed on gantt page - top level. Tags can span projects, so gantt can too.

## Comments

@falconandy here is new gantt story. Will write another for multiple tags.
sent by @mreider at 2018-07-04 02:12 PM

## Attachments


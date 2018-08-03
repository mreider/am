# Pivotal import supports user creation

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: pivotal  
Status: finished  
Assigned: falconandy  
Estimate: 2  
Finished: 2018-08-03 09:58 PM  

## Problem statement

When I import a Pivotal csv I have to create all the users separately

## Possible solution

Look at the columns in the pivotal csv that contain user names and create user files for each one.

## Comments

@falconandy - new bit
sent by @mreider at 2018-07-27 04:53 AM

@falconandy I am also noticing that "assigned" does not show the user that is assigned to the story. Do you still have the Pivotal csv?
sent by @mreider at 2018-08-02 02:22 AM

@mreider This story isn't ready yet.
sent by @falconandy at 2018-08-02 09:54 AM

@mreider Ready for testing
sent by @falconandy at 2018-08-02 11:39 AM

@falconandy it looks like there can be more than one 'owned by' column in the sheet. When I imported a sheet, it only created 3 users. I looked and there are a few colums, all called 'owned by' my guess is they are historical. You are taking the last column. Please take the first instead - it is the most recent person who owned the story (I think)
sent by @mreider at 2018-08-03 04:01 AM

@mreider fixed
sent by @falconandy at 2018-08-03 06:29 PM

@falconandy - well, it's tricky. Looks like there can be up to 3 'owned by' and the CSV sometimes has the first column empty, and only the second column populated. So I think we should do this: For 'assigned' - find the first name that appears, in whatever column. For creating users - create a user for each person in each column.

Make sense?
sent by @mreider at 2018-08-03 03:06 PM

@mreider Try new fix, please
sent by @falconandy at 2018-08-03 08:35 PM

## Attachments

## Metadata

Created: 2018-07-27 04:51 AM  
Modified: 2018-08-03 09:58 PM  
Author: Matt Reider  

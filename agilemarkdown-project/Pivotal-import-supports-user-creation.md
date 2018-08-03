# Pivotal import supports user creation

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: Pivotal  
Status: doing  
Assigned: falconandy  
Estimate: 2  

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

## Attachments

## Metadata

Created: 2018-07-27 04:51 AM  
Modified: 2018-08-02 02:11 AM  
Author: Matt Reider  

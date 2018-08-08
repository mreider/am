# Regenerate overview

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Sometimes there are things that are out of sync and force the user to do things in git that they shouldn't necessarily do. This will happen all the time when people use `am sync` since new stories might be different on different people's local copies and the overview pages will be different for each.

## Potential solution

Don't try and merge changes from the overview page, just regenerate it. This could result in a priority order change loss, but since there should be one product manager per backlog, and no engineers should change priority, it is fine.

## Comments

 @falconandy I created a cron that runs am sync. The problem is that the project and archive pages (and maybe others) are
being regenerated even when there are no changes and the modified date is causing git commits. Can you change so that we only regenerate if there is a change?

## Metadata

Created: 2018-05-02 10:26 AM  
Modified: 2018-05-22 08:49 PM  
Author: mreider  

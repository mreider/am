# Finished-stories-should-be-editable

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: cleanup  
Status: doing  
Assigned: falconandy  
Estimate: 1  

## Problem statement

Not sure what is going on - but I had a story that was marked as finished, and had a finished date. When I tried to change the assignee, in pendulum, it exited 1. Maybe this is the problem that am sync had in the other story. Unclear.

## Possible solution

## Comments

@falconandy - bug?
sent by @mreider at 2018-08-03 10:08 PM

@mreider Can't reproduce. Both on local Pendulum and on reider.club
sent by @falconandy at 2018-08-04 10:52 AM

@mreider Could you provide the story name?
sent by @falconandy at 2018-08-04 10:54 AM

@falconandy try Tags-are-not-case-sensitive.md
sent by @mreider at 2018-08-04 02:27 PM

@falconandy - and try this story in pendulum? Always exits 1?
sent by @mreider at 2018-08-04 02:28 PM

@mreider I tried with Tags-are-not-case-sensitive.md on reider.club.
I modified 'Assigned' to mreider, saved, to falconandy, saved, to falconandy555, saved, to falconandy, saved.
No errors, all saves were successful.
sent by @falconandy at 2018-08-04 07:31 PM

@mreider It seems, reider.club doesn't sync periodically - finished-stories-should-be-editable.md still has unresoveld conflicts (I've resolved them manually).
I think, a merge conflict was the reason of 'exit status 1'
sent by @falconandy at 2018-08-04 07:50 PM

@mreider I added more verbose errors to both agilemarkdown and pendulum. Maybe it can help to catch the error
sent by @falconandy at 2018-08-05 04:04 PM

## Attachments

## Metadata

Modified: 2018-08-05 04:05 PM  

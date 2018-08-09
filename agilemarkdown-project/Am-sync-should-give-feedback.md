# Am sync should give feedback

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: sync  
Status: doing  
Assigned: falconandy  
Estimate: 2  

## Problem statement

Am sync works great, but it gives no feedback about what is happening.

## Possible solution

When a user runs am sync they should see in stdout the things that are happening, in the order they are happening.

For instance:

Generating project page
Generating tag page
Generating user pages
Generating idea pages
Generating velocity graph
Creating user matt reider
Sending email to john smith
Pushing changes to git
Sync successful

Errors in git, or in sending emails, should be shown.

## Comments

@falconandy another new bit
sent by @mreider at 2018-07-27 05:52 AM

@mreider Ready for testing
sent by @falconandy at 2018-08-03 09:29 PM

@falconandy - Looks good - except the git commit exits 1 if there is nothing to commit? Makes it seem like there is an error, when there isn't. 
sent by @mreider at 2018-08-03 10:02 PM

@mreider fixed
sent by @falconandy at 2018-08-04 10:37 AM

## Attachments

## Metadata

Created: 2018-07-27 05:47 AM  
Modified: 2018-08-02 11:40 AM  
Author: Matt Reider  

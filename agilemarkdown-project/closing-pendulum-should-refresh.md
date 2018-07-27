# Closing pendulum should refresh

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: clean-things  
Status: finished  
Assigned: falconandy  
Estimate: 3  
Finished: 0001-01-01 12:00 AM  

## Problem statement

When I close pendulum, I am looking at a list of outdated information

## Possible solution

Closing pendulum should refresh the page so I can see latest changes

## Comments

@falconandy can you look into this?
sent by @mreider at 2018-07-04 03:58 AM

@mreider The issue is browser cache. To disable caching I need to modify Caddy - I have to set a few response headers (as described in https://stackoverflow.com/questions/49547/how-to-control-web-page-caching-across-all-browsers).
If it's ok, please fork the Caddy - I'll modify it. Also I can setup Travis for the fork if need. 
sent by @falconandy at 2018-07-05 08:09 PM

@falconandy really? I don't see an HTTP request to the server when I close pendulum, so why would the headers matter? When I hit refresh, the page refreshes just fine. Caddy supports header settings, so I can add them to the caddyfile.
sent by @mreider at 2018-07-05 08:36 PM

@falconandy never mind. I do see the request. I'll try to add the headers myself.
sent by @mreider at 2018-07-05 08:37 PM

@falconandy ok adding  header / {
   Cache-Control "no-store, must-revalidate"
 } to my caddyfile fixed the issue. Thanks!
sent by @mreider at 2018-07-05 08:54 PM

## Attachments


## Metadata

Created: 2018-07-04 03:56 AM  
Modified: 2018-07-05 08:54 PM  
Author: Matt Reider  

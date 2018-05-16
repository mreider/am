Title: embed caddy server  
Created: 2018-05-15 09:33 PM  
Modified: 2018-05-15 09:33 PM  
Tags: server oauth web
Author: Matt Reider  
Status: planned  
Assigned: falconandy
Estimate: 5

# Embed caddy server

## Problem statement

After trying gollum, wiki.js, and realms, it looks like the best solution for serving these markdown files is the caddyserver here:

https://caddyserver.com/

## Possible solution

I am not sure how hard it would be to embed the Caddy server inside of our binary file. It looks like you can do it here:
https://github.com/mholt/caddy/wiki/Embedding-Caddy-in-your-Go-program

It would be awesome if we could also embed some of the plugins:

This one for Google OAuth:
https://github.com/tarent/loginsrv/blob/master/caddy/README.md

This one for browsing files:
https://filebrowser.github.io/caddy/

This one for serving git repositories
https://github.com/abiosoft/caddy-git

You can serve Markdown files using Caddy here:
https://caddyserver.com/docs/markdown

You could wrap the markdown with this:
http://strapdownjs.com/

Then we can add commands to agilemarkdown to start the server, and read the caddyfile with the settings for these plugins. Either that, or we can just use the caddyserver along with agilemarkdown.

I would like you to get this set up so I can describe it via documentation and use it with GoogleAuth on a server.

The files would not be editable on that server, but I *think* that the filebrowser plugin allows for file editing. If it does, we could also run `am sync` after someone has edited a file? Have to play with that to see.

## Comments

@falconandy let me know what you think here.

## Attachments

# Integrate-pendulum

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-26 12:15 AM  
Modified: 2018-05-26 12:40 AM  
Tags:   
Author: Matt Reider  
Status: unplanned  
Assigned: falconandy  
Estimate: 5  

## Problem statement

I am serving these files at https://reider.club - I use the caddy server. I also use pendulum to edit the files. You can see how I set this up by
looking at the [README](https://github.com/mreider/agilemarkdown/blob/master/README.md) file.

I incorporated [Pendulum](https://github.com/titpetric/pendulum) into the project so that people can edit files via browser. To access pendulum, the
user needs to authenticate, and then browse to https://reider.club:666 - you can test this on your own.

There are a few problems I would like you to think about and make some suggestions.

1. When a user is on a page - they do not know that the page is editable unless they browse to that-page:666
2. When a user is done editing - they do not know how to go back to the normal view of the page without typing that-page (no port).
3. Adding ideas would be done with pendulum, but there is no way to link there from the ideas page
4. New stories do not get generated using pendulum - the story is just blank, like any file, without the proper format (metadata, headers, etc)
5. After a new story or idea is created there is no way to sync, except via crontab, which might be ok?

## Possible solution

If we could create a config file like `.config` we could add `use-pendulum:true` which would create a pendulum link at a certain port.
That link could go on every page, which would invoke pendulum edit view for the page.

If you can hack pendulum source code, and create a custom version of it, we could add links to the top for going back to agilemarkdown view (no port),
plus links to go back to the home page and project view (maybe?). Not sure if you can hack this thing easily or not.

If you can hack pendulum source code, and create a custom version of it, you could also create new stories that follow our template.

If use-pendulum:true is om the config, we could also add a new button to the menu "add idea" which would go to pendulum to create a new file, with the
right template for ideas - since it's different than stories (with rank?)

If you can haack pendulum, it would be interesting to add a button to sync.

## Comments

@falconandy - let me know if this is crazy or not - or if you have other ideas

## Attachments

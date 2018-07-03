# Stories can be archived

Project: Agilemarkdown-project

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [velocity](../velocity.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-10 11:43 AM  
Modified: 2018-05-22 08:49 PM  
Author: Matt Reider  
Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

The list of finished stories, and things that sit in 'unplanned' will get quite long. We would like to put them somewhere, but not have them clutter things up.

## Potential solution

Add new key to story metadata "archive: 1" (can be "true")

Add a new directory under the project folder, called 'archive' - this will be a special name that cannot be overwritten via 'create-backlog' (throw an error if someone tries to use `am create-item archive`).

In this directory we will move any file that has the `archive:1` key-pair. There will also be a new file in the project directory called `archive.md` that is exactly the same as the project file in how it shows lists of work, and preserves the order of each list.

When a user changes the key `archive:1` to `archive:0` or false, or deletes that key completely, then the file will be moved BACK into the main project folder, and regenerates the project page, as well as the archive page.

A link to the archive page should go at bottom of the project page as follows:

```
(Archived stories)[link to archive page]
```
## Comments

 @mreider Ready for testing. There is a chance of some regression.

 @mreider Should 'work', 'change-status', 'assign' commands show all items or only active (non archived)?

  @falconandy once something is archived it should not show up in any lists. If user wants to "unarchive" they can move it manually

# Tags have their own pages

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Users will want to see which stories are tagged and look at a list by tag. These users will not have access to command line tools.

## Potential solution

Let's add a new directory under the root folder, called 'tags' - this will be a special name that cannot be overwritten via 'create-backlog' (throw an error if someone tries to use `am create-item tags`).

In this directory, there will be generated files (generated when the user does am sync) that show a list of all the stories that have a certain tag.

THESE PAGES SHOW TAGS ACROSS BACKLOGS.

So if there is a tag 'colors' - a file will be generated in the tags directory called 'colors.md' with all of the stories in a list:

```
# Story list for tag: colors

MARKDOWN TABLE
(show markdown tables that are similar to work -t tag, but with links to the stories and is ACROSS BACKLOGS - not just for one backlog. Show the project, also, in the table.)

```

Go ahead and regenerate this page with every sync, so we can avoid problems like the overview page has.


## Comments

 @mreider Should the list be grouped by story status?
 @falconandy yes, sounds great.
 @falconandy test

 @mreider Should the list show archived stories?
 @falconandy no

 @mreider Is "the reorganizing" the second way to change story priority? How it should work together if stories order is changed both in overview and tags pages?
 @falconandy ok, my mistake. too complicated. Let's have them appear in order of modified? Is that ok?
 @mreider Ok. Small detail - Ascending or Descending?

 @falconandy descending

 @falconandy this page also needs the same menu items at the top and in the same format as the others.

 @mreider The tag pages are not related to a specific project. I can't add the 'project page' link, only links to all related projects. 

 @falconandy this has an issue with tags from Pivotal Tracker. It looks like Pivotal separates tags with commas, but allows tags with spaces in them. If you could fix the import to replace the space with a dash, and then treat each comma separated tag as a different tag that would be great.

## Metadata

Created: 2018-05-10 11:31 AM  
Modified: 2018-05-22 08:49 PM  
Author: Matt Reider  

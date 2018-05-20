# Tags have their own pages

Created: 2018-05-10 11:31 AM  
Modified: 2018-05-18 08:46 PM  
Author: Matt Reider  
Status: doing  
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

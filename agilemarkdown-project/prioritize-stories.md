# Prioritize stories

[project](../agilemarkdown-project.md) [archive](archive.md) [index](../index.md) [ideas](../ideas.md) [tags](../tags.md)

Created: 2018-05-22 04:10 PM  
Modified: 2018-05-22 04:10 PM  
[home](../index.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md) || [idea list](../ideas.md) || [tag list](../tags.md)

Created: 2018-05-02 11:44 AM  
Modified: 2018-05-22 07:44 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Stories at the gate, and in the hangar, should be stack ranked, so that the most important thing is at the top of the list. Without some kind of rank order, it won't be clear what is important and should be worked on next.

## Possible solution

When a user changes the order of a story in the overview page, the order should be preserved. Any new story that is moved using change-status should automatically go to the bottom of the list in that section.

When a user types a command from the command line like `am work` or `am change-status` the list of stories will be in the same order as the overview page.

## Comments

 @falconandy - this works great.

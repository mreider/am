# Regenerate overview
  
Created: 2018-05-02 10:26 AM  
Modified: 2018-05-10 08:41 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Sometimes there are things that are out of sync and force the user to do things in git that they shouldn't necessarily do. This will happen all the time when people use `am sync` since new stories might be different on different people's local copies and the overview pages will be different for each.

## Potential solution

Don't try and merge changes from the overview page, just regenerate it. This could result in a priority order change loss, but since there should be one product manager per backlog, and no engineers should change priority, it is fine.

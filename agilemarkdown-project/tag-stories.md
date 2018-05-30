# Tag stories

Project: Agilemarkdown-project

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-02 02:16 PM  
Modified: 2018-05-22 08:49 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 5  

## Problem statement

## Potential solution

Stories will have tag values like this:
```
Title: this thing is awesome
Created: 2018-04-30 02:08 PM
Modified: 2018-04-30 02:21 PM
tags: this that the_other_thing
Author: mreider
Status: doing
Assigned: jimmy
Estimate: 2
```

A user can show work with -t and a list of tags

```
am work -t this that the_other_thing
```

Please add tags to the markdown tables for for 'am work' and 'am points'

## Comments

 @mreider Ready for testing

 @falconandy it looks like this does not work am work -s p -t "foo oauth" - I thought I said this should be an "OR" ? Are you treating it like an "AND"?

 @mreider You wrote in Upwork chat "let's use quotes if there's more than 1. and it's an AND"
I'll change it to OR

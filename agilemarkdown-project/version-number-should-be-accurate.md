# Version number should be accurate

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-17 09:57 PM  
Modified: 2018-05-24 10:21 PM  
Tags:   
Author: Matt Reider  
Status: doing  
Assigned: falconandy  
Estimate:   

## Problem statement

When I type am --version it is always 0.0.0

## Possible solution

Is there a way you can increase the version number each time with each commit?

## Comments

@mreider I've added build.sh script to build/install the binary with version info equal to UTC date/time of the last git commit (like 2018.05.24.181642)
Based on [https://stackoverflow.com/questions/11354518/golang-application-auto-build-versioning]()

## Attachments

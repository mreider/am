# Pivotal-tracker-import

[home](../index.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md) || [idea list](../ideas.md) || [tag list](../tags.md)

Created: 2018-05-22 04:10 PM  
Modified: 2018-05-22 04:22 PM  
[home](../index.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md) || [idea list](../ideas.md) || [tag list](../tags.md)

Created: 2018-05-02 02:10 PM  
Modified: 2018-05-22 07:44 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 2  

# Problem statement

An existing Pivotal Tracker story should be imported into an agilemarkdown project

## Potential solution

'am import filename.csv'

Title-->Title

Labels-->Tags

Current State ---> Status -- parsed by: (accepted = finished) (delivered, finished, started = doing) (unstarted = planned) (unscheduled = unplanned)

Owned by ---> assigned

Estimate ---> estimate

Requested by ---> Author

Description ---> (this is the body of the file, underneath all the metadata)

Someday, maybe, we can build importer for other things (JIRA, Trello, etc.)

Here's a [CSV for a sample project](https://docs.google.com/spreadsheets/d/1e4rmJksVa9mXTRYNAFuaJ7ICcHOilvGBiucnmDsSo8w/edit?usp=sharing)

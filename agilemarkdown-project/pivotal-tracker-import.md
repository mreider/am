# Pivotal-tracker-import

[project](../agilemarkdown-project.md) [archive](archive.md) [index](../index.md) [ideas](../ideas.md) [tags](../tags.md)

Created: 2018-05-02 02:10 PM  
Modified: 2018-05-20 08:02 PM  
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

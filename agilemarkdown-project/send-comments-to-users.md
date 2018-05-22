# Support for clarification requests

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-03 03:32 PM  
Modified: 2018-05-22 08:49 PM  
Author: mreider  
Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

There is no way to show users what comments are waiting for their responses.

## Possible solution

We could add a comment section to each story, and in the overview page we could show the things that people need to respond to.

```

## Comments
@falconandy I think the problem here is that things are hard.
```

The next time a user does 'am sync' the comment will list this users with unanswered comments:

```
Title: agilemarkdown-project  
Created: 2018-05-02 10:25 AM  
Modified: 2018-05-07 01:55 PM

## Clarifications
User |  Excerpt | Story |
---|---|---|
@falconandy | I think the problem... | [pivotal-tracker-import](pivotal-tracker-import) |

## Stories

### Doing
 User | Title | Points
---|---|:---:
 falconandy | [pivotal-tracker-import](pivotal-tracker-import) |  

### Planned
 User | Title | Points
---|---|:---:
 falconandy | [regenerate overview](regenerate_overview) |  

```

To close out a comment, you can just put a tab or a space in front of the username

```
  @username I think the problem here is that things are hard.
```

This will take it off the clarifications section - it will nolonger appear there.

## Comments

  @mreider Max size for the "Excerpt" column is 100. Is it fine?
  @falconandy Looks good to me!

## Attachments

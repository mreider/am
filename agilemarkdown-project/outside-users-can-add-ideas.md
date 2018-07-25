# Outside users can add ideas

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Status: finished  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Users that are not on the product / engineering team would like to add ideas to our backlogs. They don't know git, they don't use the command line.

After they add an idea, they want to see it progress.

## Potential solution

Let's add a new directory under the root folder, called 'ideas' - this will be a special name that cannot be overwritten via 'create-backlog' (throw an error if someone tries to use `am create-item ideas`).

In this directory, any user can drop a markdown file (must have .md extension). And write whatever they want to add. For instance, this could be in /folder/ideas/paint-colors.md

Note that this will be done using the web interface, so the user doesn't need to run any commands or sync. It will be in the Git repo automatically.

```
I think it would be cool to paint the house blue, and the dorr white, rather than the door blue, and the house white.
```

The next time someone runs am sync, this file will be parsed. A timestamp will be placed at the top as follows:

```
Title: Paint colors  
Created: 2018-05-10 11:14 AM  
Modified: 2018-05-10 11:14 AM
Author: Matt Reider
Tags:
```

A file in the root directory, with all the product overviews, will be named ideas.md and it will show a list of all ideas as follows.

```
Author | Idea | Tags |
---|---|---|---|
Jimmy | (idea name)[ideas/idea-link.md](pivotal-tracker-import) | (tag1)[tag-page] (tag2)[tag2-page] |

```

## Comments

  @falconandy this works perfectly!

  @falconandy sorry, can you also add a header to this page # Ideas

 @falconandy the idea link is broken on the idea page because there is nothing printing inside of ``[here](but this is fine)`` this is also happening on the index page. I think this is because it was grabbing titles from the title key/pair not the header.

 @falconandy it also looks like we are creating the menu links and dates over and over again. see here: https://reider.club/project/ideas/some-things.md

## Metadata

Created: 2018-05-10 11:14 AM  
Modified: 2018-05-22 08:49 PM  
Author: Matt Reider  

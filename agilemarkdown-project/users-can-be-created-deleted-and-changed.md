# Users can be created, deleted and changed

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: users  
Status: doing  
Assigned: falconandy  
Estimate: 3  

## Problem statement

Deleting a user has to be done manually, and every story must be changed.

## Possible solution

There should be a command ‘am create-user’ with arguments for a username and email. Username should support spaces (quotes?). If that user file already exists, give an error.

There should be a command ‘am delete-user’ with argument for username, or email, or email prefix (prefix@domain.com). If none of these can be found, give an error. Also confirm (are you sure?). This will also remove that user from every story he is assigned to.

There should be a command ‘am change-user’ with old user (name, email, or prefix) and new user (name, email, or prefix). This change all assigned user stories from the old user to the new user.

## Comments

@falconandy another one.
sent by @mreider at 2018-07-27 05:43 AM

@mreider Ready for testing
sent by @falconandy at 2018-08-01 08:40 PM

@falconandy not sure this is working as we want. See below:

am create-user --name foo --email foo@foo.om
ubuntu@ip-172-26-1-7:~/reider.club$ cd users/
ubuntu@ip-172-26-1-7:~/reider.club/users$ ls
Andrey Sokolov.md  foo@foo.om.md  Matt Reider.md
ubuntu@ip-172-26-1-7:~/reider.club/users$ cat foo@foo.om.md
sent by @mreider at 2018-08-02 02:07 AM
# foo@foo.om

Email: foo

## Attachments

## Metadata

Created: 2018-07-27 05:34 AM  
Modified: 2018-07-30 08:42 AM  
Author: Matt Reider  

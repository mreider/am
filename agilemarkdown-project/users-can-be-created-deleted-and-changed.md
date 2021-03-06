# Users can be created, deleted and changed

Project: Agilemarkdown-project

[home](../index.md) • [idea list](../ideas.md) • [tag list](../tags.md) • [velocity](../velocity.md) • [timeline](../timeline.md) • [users](../users.md) • [project page](../agilemarkdown-project.md) • [archive](archive.md)

Tags: users  
Status: finished  
Assigned: falconandy  
Estimate: 3  
Finished: 2018-08-03 04:04 AM  

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
foo@foo.om
Email: foo
sent by @mreider at 2018-08-02 02:07 AM

@mreider Misprint. Fixed.
Sorry, I forgot to mention - you could use more simple command:
am create user foo foo@foo.om
am create user John Green john@foo.om
--name and --email flags were for Pendulum, I've hidden them
sent by @falconandy at 2018-08-02 10:10 AM

@falconandy also - it looks like am delete-user foo won't work, but am delete-user foo@foo.om works. I was thinking both would work. The change-user command works perfectly, thanks.
sent by @mreider at 2018-08-02 02:12 AM

@mreider It works for me. Could you try with updated am, please? 
sent by @falconandy at 2018-08-02 10:10 AM

@falconandy works. Thanks.
sent by @mreider at 2018-08-03 04:04 AM

## Attachments

## Metadata

Created: 2018-07-27 05:34 AM  
Modified: 2018-08-03 04:04 AM  
Author: Matt Reider  

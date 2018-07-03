# Proper-clarifications-and-ideas

Project: Agilemarkdown-project

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [velocity](../velocity.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-26 12:31 AM  
Modified: 2018-06-05 10:41 PM  
Tags:   
Author: Matt Reider  
Status: doing  
Assigned: falconadny  
Estimate: 5  

## Problem statement

People shouldn't have to visit the project to clarify or follow ideas - things should come through email

## Possible solution

Create a file .config that correlates usernames with emails like this:

`mreider mreider@gmail.com, falconandy andreyso@gmail.com` etc. or whatever format you think is best.

Also in the config are SMTP address, port and credentials.

When a comment is made in a file `@mreider I think you are smelly` the next time we do an am sync, and email will be sent to mreider from
the current user. If the user is web based, we need to figure out a way to pass the email from the caddy server to am sync... ideas?

Then we need to get rid of the clarifications list, those clarifications will go to people's inbox.

After am sync is done, it will put a 'sent by @some-user at [timestamp]' on the line after the comment, followed by a line break.

If that line is not there, am sync will send the email. If that line is there, am sync knows the email was already sent.

No need to ignore comments with spaces before the @mreider - this functionality can be deleted. The line / timestampt is how we ignore now.

Clear?

## Comments

@mreider Ready for testing.

`.config.json` should be filled (the dot to hide the config file in Pendulum):
```
{
  "SmtpServer": "SMTP_SERVER:PORT",
  "SmtpUser": "USER_NAME",
  "SmtpPassword": "PASSWORD",
  "RemoteGitUrlFormat": "%s/blob/master/%s"
}
```

Fresh Agilmarkdown and Pendulum are required.
sent by @falconandy at 2018-06-05 10:41 PM


## Attachments

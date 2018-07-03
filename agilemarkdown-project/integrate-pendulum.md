# Integrate-pendulum

Project: Agilemarkdown-project

[home](../index.md) || [idea list](../ideas.md) || [tag list](../tags.md) || [velocity](../velocity.md) || [project page](../agilemarkdown-project.md) || [archive](archive.md)

Created: 2018-05-26 12:15 AM  
Modified: 2018-06-05 10:33 PM  
Tags:   
Author: Matt Reider  
Status: doing  
Assigned: falconandy  
Estimate: 5  

## Problem statement

I am serving these files at https://reider.club - I use the caddy server. I also use pendulum to edit the files. You can see how I set this up by
looking at the [README](https://github.com/mreider/agilemarkdown/blob/master/README.md) file.

I incorporated [Pendulum](https://github.com/titpetric/pendulum) into the project so that people can edit files via browser. To access pendulum, the
user needs to authenticate, and then browse to https://reider.club:666 - you can test this on your own.

There are a few problems I would like you to think about and make some suggestions.

1. When a user is on a page - they do not know that the page is editable unless they browse to that-page:666
2. When a user is done editing - they do not know how to go back to the normal view of the page without typing that-page (no port).
3. Adding ideas would be done with pendulum, but there is no way to link there from the ideas page
4. New stories do not get generated using pendulum - the story is just blank, like any file, without the proper format (metadata, headers, etc)
5. After a new story or idea is created there is no way to sync, except via crontab, which might be ok?

## Possible solution

If we could create a config file like `.config` we could add `use-pendulum:true` which would create a pendulum link at a certain port.
That link could go on every page, which would invoke pendulum edit view for the page.

If you can hack pendulum source code, and create a custom version of it, we could add links to the top for going back to agilemarkdown view (no port),
plus links to go back to the home page and project view (maybe?). Not sure if you can hack this thing easily or not.

If you can hack pendulum source code, and create a custom version of it, you could also create new stories that follow our template.

If use-pendulum:true is om the config, we could also add a new button to the menu "add idea" which would go to pendulum to create a new file, with the
right template for ideas - since it's different than stories (with rank?)

If you can haack pendulum, it would be interesting to add a button to sync.

So we could have three new buttons next to the current "new file" button - sync, new story, new idea.

and then a few buttons for navigating back to the normal page etc

## Comments

 @falconandy - let me know if this is crazy or not - or if you have other ideas

 @mreider I think, we could suggest to use a custom Caddy template file if Pendulum should be used.
For example, the template below has 4 additional lines to add 'EDIT' link (only for stories and projects) - you could test it, it should work:
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Agilemarkdown</title>
  <meta charset="utf-8">
  <link rel="stylesheet" href="https://example.org/css/styles.css">
</head>
<body body style="margin:20px;padding:20px">
<br>

{{if or (eq .URI "/") (eq .URI "/index.md") (eq .URI "/ideas.md") (eq .URI "/tags.md") (.PathMatches "/tags/") (.PathMatches "/ideas/")}}
{{ else }}
<a href="https://{{.Host}}:666/edit{{.URI}}">EDIT</a>
{{end}}

<div class="container">
  {{.Doc.body}}
</div>

</body>
</html>
```

 @mreider I've looked at the Pendulum source code. It seems, it could be forked and customized to our needs.

 @falconamdy - I will fork and add you

@mreider See the next section "Proof of concept"
sent by @falconandy at 2018-06-05 10:33 PM

## Proof of concept

### Sample template file (for Caddy)

New links (buttons) to 'Edit' (available on project, story and idea pages), 'Add story' (available on project, story and archive pages) and 'Add Idea' (available on all pages)

Additional css for link panel (class 'nav')

Link part 'https://{{.Host}}:666/' should be modified if need (http/https, port)

```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Agilemarkdown</title>
  <meta charset="utf-8">
  <link rel="stylesheet" href="https://example.org/css/styles.css">
<style>
.nav {
  position: absolute;
  top: 0;
  right: 0;
  margin: 5px;
}
</style>
</head>
<body body style="margin:20px;padding:20px">
<div class="nav">
{{if or (eq .URI "/") (eq .URI "/index.md") (eq .URI "/ideas.md") (eq .URI "/tags.md") (.PathMatches "/tags/")}}
{{ else }}
  <a href="https://{{.Host}}:666/edit{{.URI}}">Edit</a>
{{if not (.PathMatches "/ideas/")}}
  <a href="https://{{.Host}}:666/addStory{{.URI}}">Add story</a>
{{end}}
{{end}}
  <a href="https://{{.Host}}:666/addIdea">Add idea</a>
</div>
<div class="container">
  {{.Doc.body}}
</div>

</body>
</html>
```

### Custom Pendulum Binary

```
cd ~/go/src/github.com
mkdir titpetric
cd titpetric
git clone https://github.com/mreider/pendulum-agilemarkdown pendulum
cd pendulum
go get -u github.com/jteeuwen/go-bindata/...
./build_all.sh
```

Then use a binary for your OS from build/ subfolder instead of standard version. 

### Agilemarkdown Binary

Fresh Agilemarkdown binary should be put to the same folder where Pendulum binary is.

### Run

Run Caddy

Run custom Pendulum

New links should work

### Issues

A Caddy user should be passed to Pendulum to be used as an author of stories/ideas

## Attachments

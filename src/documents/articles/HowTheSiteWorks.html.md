```
title: How the site works
layout: article
tags: ['why?','article']

```

### static websites
A Static website consists of pages. Each page contains all of its content. Thus each page is really just a file. Unlike 'dynamic' data-driven sites there is no separate database.

**Important: Template Configuration -> template data -> where you can configure data and helpers for use in your templates.

Navigating through the site simply loads html pages from a directory and displays them in the browser.

These files are generated by the static site generator. So, all editing is done on static files using a server-side templating language. These templates are then used to generate html and it is this html that you view in the browser.
this means that in order to deploy a static website you just need to get the html, css and javascript onto the server. Any server capable of serving static files will do the job. 

But in order to create the files in the first place you do need the generator component on your machine.  Or you can put it on a server. Either way

What happens if you put a html file in the output folder? the rest of the site will not know how to call it.
You can reference javascript from your files. So you should be able to do javascript tasks that involve data or anything else.

The 'design' of the site is managed through 'layouts'. Layouts are basically templates that can contain custom logic to determine 
Layouts.
Layouts are used to customise the context in which different content types are displayed.
Layouts can be nested in an heirarchical structure if needed.
<img src="~/files/images/iphone.png">

Can you have interaction with a static site? 

There is usually one 'root' layout, in this case "default.html.eco", which provides the 'Shell' of the site. The shell is meant to provide the 'global' elements that are needed by all 'pages' of the site.All other layouts will be nested within this shell 
Here we include a global navigation bar and a global footer.
The layout contains a "Content" placeholder. This area will be populated with the contents of the posts, articles or other content that you create.

We can think of this content placeholder as a host for 'pages' that we create to present specific content types. So, we can have a 'posts-page' template which will allow us to create a specific layout for displaying posts.
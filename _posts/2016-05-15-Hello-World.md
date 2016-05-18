---
layout: post
title:  "Hello World"
date:   2016-05-15 19:32:00 -0400
categories: jekyll introduction
comments: true
analytics: false
---

Markdown (or Textile), Liquid, HTML & CSS go in. Static sites come out ready for deployment.
<!--more-->

#### Headings

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

#### Blockquote

> No more databases, comment moderation, or pesky updates to install—just your content.


#### Unordered List

*   Jekyll
*   Ruby
*   Markdown
*   Liquid

#### Ordered List

1.  Jekyll
2.  Ruby
3.  Markdown
4.  Liquid

#### Link

This is [an example](http://example.com/ "Title") inline link.

#### Paragraph w/ strong, em, etc.

These are just a few of the _available_ **configuration** options. Many configuration options can ~~either~~ be specified as flags on the <abbr title="Command Line Tool">command line</abbr>, or alternatively (and more commonly) they can be specified in a _config.yml file at the root of the source directory. Jekyll will [automatically use](http://joro.me/) the options from this file when run. For example, if you place the following lines in your _config.yml file.

#### Image

<div markdown="block">![](https://images.unsplash.com/photo-1449452198679-05c7fd30f416?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&s=73181f1c6d56b933b30de2bfe21fdf3b)</div>

Photo by [Rachel Davis](https://unsplash.com/rmaedavis).

#### Video

<div class="fluid-width-video-wrapper" style="padding-top: 56.25%;"><iframe src="https://www.youtube.com/embed/iWowJBRMtpc" frameborder="0" allowfullscreen="" name="fitvid0"></iframe></div>

### Code Blocks

#### Inline Code Blocks

This is an example of an `inline code block`

#### Default Code Block

```
This is code blog.

```

#### Fenced Code Blocks

```
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

#### Alternate Fenced Code Blocks

##### Syntax Aware Code Blocks

~~~ javascript
var s = "JavaScript syntax highlighting";
alert(s);
~~~
 
~~~ python
s = "Python syntax highlighting"
print s
~~~

~~~ ruby
def what?
  "Ruby syntax"
end
~~~

#### Definition Lists

<dl>

<dt>Definition Title</dt>

<dd>Definition Description</dd>

</dl>

#### Paragraphs w/ Aligned Images

The Jekyll gem makes a jekyll executable available to you in your Terminal window. You can use this command in a number of ways.

![test](https://images.unsplash.com/photo-1432821596592-e2c18b78144f?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&s=3f9c78df0edb464244bbabb04d1797d8){:class="svg-filter"}

Photo by [Dustin Lee](https://unsplash.com/dustinlee).


This site aims to be a comprehensive guide to Jekyll. We’ll cover topics such as getting your site up and running, creating and managing your content, customizing the way your site works and looks, deploying to various environments, and give you some advice on participating in the future development of Jekyll itself.

Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

![](https://images.unsplash.com/photo-1442037025225-e1cffaa2dc23?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&s=7fe04b68b0cb123bf568c6951c14b177)

Throughout this guide there are a number of small-but-handy pieces of information that can make using Jekyll easier, more interesting, and less hazardous. Here’s what to look out for.

If you come across anything along the way that we haven’t covered, or if you know of a tip you think others would find handy, please file an issue and we’ll see about including it in this guide.

The front matter is where Jekyll starts to get really cool. Any file that contains a YAML front matter block will be processed by Jekyll as a special file. The front matter must be the first thing in the file and must take the form of valid YAML set between triple-dashed lines.

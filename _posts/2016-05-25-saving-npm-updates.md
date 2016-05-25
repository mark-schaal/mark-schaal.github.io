---
layout: post
title:  "Saving Package Updates with NPM"
date:   2016-05-25 17:00:00 -0400
categories: tips-and-tricks node.js
comments: true
analytics: false
permalink: /articles/tips-and-tricks/node/saving-npm-updates
---

Today I am going to take a quick look at how we manage Node.js projects and dependencies with the Node Package Manager (NPM). Specifically, we want to ensure that our package.json file is consistently kept up-to-date with any changes we make from the command line, and that any time our packages receive updates from the central repository, those changes are synchronized and reflected with our project.
<!--more-->

## Overview

>"(...)npm-check-updates is a command-line tool that allows you to upgrade your package.json or bower.json dependencies to the latest versions, regardless of existing version constraints." - <https://github.com/tjunnone/npm-check-updates> 

## Requirements and Usage

We are going to use the npm-check-updates command line utility to both check for updates to our existing packages, and save any updates to the package.json file.

In order to do this, we need to first install the npm-check-updates CLI using the same process as we would for any other NPM module:

**Installing npm-check-updates**

~~~ javascript
$ npm install -g npm-check-updates;
~~~

Now that we have the package installed, let's get into how you can use this tool to optimize your development lives.

**Checking for package updates with NPM:**

Running `npm-check-updates` by itself will create a status list:

~~~ 
$ npm-check-updates;
	
gulp-autoprefixer  ^2.3.1  →          ^3.1.0 
gulp-sass-glob      0.0.8  →           1.0.6 
kss                ^2.4.0  →  ^3.0.0-beta.14 
~~~

Alternatively, we can use the short form alias for this command:

~~~ 
$ ncu;
~~~

**Saving package updates to our package.json file with NPM:**

~~~ 
$ npm-check-updates -u;
~~~
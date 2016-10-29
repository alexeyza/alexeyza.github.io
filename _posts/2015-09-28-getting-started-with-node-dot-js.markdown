---
layout: post
title: "Getting Started with Node.js"
date: 2015-09-28 13:21:02 -0700
comments: true
published: true
categories: ['Node.js', guide]
---
<img style="float:left; margin: 8px 20px" src="/assets/article_images/2015-09-28-getting-started-with-node-dot-js/nodejs.png" widht="180" height="180" title="Node.js"/>

The [Node.js](https://nodejs.org/en/) project and its community have undergone major changes in recent years, among which is the forking of the project (and perhaps the community itself). This situation causes confusion for newcomers, who find themselves with compatibility issues and difficulties in setting up a working and up-to-date environment.

In this post, I show how to get the recent version of Node.js on a Linux OS in an easy way.

<!--more-->

## What is Node.JS?
Node.js is an event-driven I/O **server-side** (backend) JavaScript environment based on Chrome's V8 JavaScript engine. It is considered a very popular backend environment, and it uses [NPM](https://www.npmjs.com/), the best package manager in my opinion (however, we'll leave the discussion on what makes NPM so good for a different post).

At some point, Node.js [was forked](http://anandmanisankar.com/posts/nodejs-iojs-why-the-fork/) into two projects: **Node.js** and **IO.js**, causing compatibility issues and disputes in the community. While recently, these projects have been [merged back](http://www.infoworld.com/article/2960452/javascript/unforked-iojs-v3-sets-stage-for-nodejs-merger.html) with Node v4.x.

However, not everyone have caught on with the recent changes (which at some point should be a thing of the past). My OS of choice, Ubuntu, only supports [Node.js 0.12.7](https://nodejs.org/en/download/releases/) through the official repositories. Where version 0.12.7 is the latest stable version **prior** to the forking of the project. Thus, the best way to get the current version of Node.js on Linux is through [NVM](https://github.com/creationix/nvm).

## Removing the older version of Node
First, create a **backup** list of the previously globally installed NPM packages:

```bash
npm ls -gp > node_packages.txt
```

If you installed Node.js through `apt-get`, uninstall by using the following:

```bash
sudo apt-get remove nodejs
```

Additionally, your home folder may contain a `.npm` folder that can be removed (since NVM will use its own path for NPM packages).

## Installing Node.js with NVM
Grab the latest copy of NVM (you may need to `sudo apt-get install curl` first):

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.27.1/install.sh | bash
```

Update NVM to latest version:

```bash
cd ~/.nvm
git pull origin master
```

Then restart your terminal window, and install the latest Node version:

```bash
nvm install stable
```

or if you want a specific version (e.g., version 4.1.1):

```bash
nvm install 4.1.1
```

And tell NVM which version of Node you want to use (when a specific version is needed):

```bash
nvm use 4.1.1
```

Define a default version, so that you don't have to pick a Node version each time you start your terminal. This will **activate** the specified version each time the terminal starts, and it will do it **silently**.

```bash
nvm alias default stable
```

And lastly, check the installed version of Node:

```bash
node --version
```

When updating to a newer version:

```bash
nvm ls
nvm install stable
nvm ls
nvm uninstall 4.1.1
```

If later on you encounter errors with installing packages _globaly_, make sure your `NODE_PATH` is defined. You can do so by adding the following to `~/.bashrc` or `~/.zshrc`:

```
export NODE_PATH=$NODE_PATH:/home/alexeyza/.nvm/versions/node/v4.1.1/lib/node_modules
```

* * *
The above steps are mostly based on a Stack Overflow [answer](http://askubuntu.com/questions/672994/how-to-install-nodejs-4-on-ubuntu-15-04-64-bit-edition/673046#673046) and the NVM [docs](https://github.com/creationix/nvm), with minor changes to make it more sustainable for future updates.
---
layout: post
title: "Setting up a Go Development Environment with Sublime Text"
date: 2016-09-28 15:44:18 -0700
comments: true
published: true
categories: [Go, guide, 'Sublime text']
---
<img style="float:left; margin: 8px 20px" src="/assets/article_images/2016-09-28-setting-up-a-go-development-environment-with-sublimetext/gogo.png" widht="180" height="180" title="Go!"/>

I really love the [Go](https://golang.org/) programming language, it feels like a mix of the best of Java and Python together. But I found that setting a Go development environment can be slightly tricky, mostly in figuring out how to set up the proper path variables.

Here, I provide a short guide on how to set up a Go development environment with Sublime Text 3 on Ubuntu/Linux. I hope it saves you (and my future-self) time when installing, updating, or re-installing the development environment.

<!--more-->

## Installing / Updating Go
If you're updating a previously installed Go version, you must first delete the older one:

```
sudo rm -r /usr/local/go
```

Download the latest version of Go archive from [https://golang.org/dl/](https://golang.org/dl/) and extract it:

```bash
sudo tar -C /usr/local -xzf go1.7.1.linux-amd64.tar.gz
```

Note: some people use the Go version manager ([GVM](https://github.com/moovweb/gvm)) to install and set up Go, a tool similar to [NVM](https://github.com/creationix/nvm) which I highly recommend for Node.js, but for Go I prefer to set up everything myself.

Next, set the PATH environment variables by adding the following to `.bashrc`:

```
export PATH=$PATH:/usr/local/go/bin
export GOPATH=$HOME/go
```

Here I use `home/alexeyza/go` as my workspace (which is `$HOME/go`), but feel free to change it according to your preference.

And, create your workspace:

```bash
mkdir -p ~/go/src/github.com/alexeyza
```

## Setting up Sublime Text
Sublime text is my editor of choice for many things, and I highly recommend it for Go. If you don't have it installed, start by installing [Sublime Text 3](http://www.webupd8.org/2013/07/sublime-text-3-ubuntu-ppa-now-available.html), and installing the [Package Control](https://packagecontrol.io/installation) plugin.

Install [GoSublime](https://github.com/DisposaBoy/GoSublime) through package control (`CTRL+Shift+P`). It's a Sublime Text plugin that provides Go code completion and other IDE-like features.

Next, set up the PATH environment variables for Sublime Text. This setting has slightly changed over time (which is why you may find different instruction variations online), but my current set up works with the following settings in `Preferences -> Package Settings -> GoSublime -> Settings-User`.  
Make sure the GOPATH matches the path configured earlier.

```json
{
    "env": {
        "GOPATH": "$HOME/go",
        "GOROOT": "/usr/local/go"
    }
}
```

Now, save and restart Sublime Text. When you first restart Sublime Text after installing GoSublime, it may take a few seconds to install and set up MarGo.

## Building and Running Go code
You can build, compile, and run your code directly from Sublime Text. Use `CTRL+B` or `CTRL+9` like so:  

![Compiling and running within Sublime Text example](/assets/article_images/2016-09-28-setting-up-a-go-development-environment-with-sublimetext/go_hello_world.gif)

For additional help, type `# help` in the Sublime Text console.

## Useful Go Plugins
Popular Go plugins that work well with GoSublime are [GoOracle](https://github.com/waigani/GoOracle), [GoImports](https://godoc.org/golang.org/x/tools/cmd/goimports), and [GoDoc](https://godoc.org/golang.org/x/tools/cmd/godoc).

You can install them with:

```bash
go get -u golang.org/x/tools/cmd/oracle
go get -u golang.org/x/tools/cmd/goimports
go get -u golang.org/x/tools/cmd/godoc
```

Read more [here](https://www.wolfe.id.au/2015/03/05/using-sublime-text-for-go-development/) on how to configure these plugins to work with GoSublime.

## Update: An Up and Coming Go IDE
There is a new and cool looking Go IDE, [Gogland](https://www.jetbrains.com/go/), created by Jetbrains (the company behind the awesome [IntelliJ](https://www.jetbrains.com/idea/) and [PyCharm](https://www.jetbrains.com/pycharm/)). Check out the early build on their website.
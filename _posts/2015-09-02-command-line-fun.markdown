---
layout: post
title: "Command Line Fun"
date: 2015-09-02 15:42:19 -0700
comments: true
published: true
categories: ['command line', scripts, hacks]
---
I recently discovered a superb [podcast on startups](http://www.shavua.net/) (in Hebrew). And, I wanted to download the episodes, so that I can listen to it when I commute to work. The podcast homepage has a page for each episode, with a download link at the bottom.

However, instead of downloading each episode manually, I decided to find an easier way, with the use of the command line. And to make it more interesting, I wanted to accomplish this with a single command line.

```bash
wget -q -O - "$@" http://simplecast.fm/podcasts/173/rss | grep -o "http://.*.mp3" | xargs wget
```

The first part brings the content, in quiet mode, to allow piping into `grep`. The second part extracts the episode file names and paths, in my case they are all mp3 files. And the last part downloads all the files. I used the RSS feed instead of the podcast homepage as a way to have all the content in a single file.

I wonder, can this be done with a single `wget` command?

BTW, a useful tool for experimenting with regular expressions is [RegExr](http://regexr.com/).
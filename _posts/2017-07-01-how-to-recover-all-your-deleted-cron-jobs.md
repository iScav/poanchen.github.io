---
layout: post
title: "How to recover all your deleted cron jobs?"
author: PoAn (Baron) Chen
author_url: https://github.com/poanchen
date: 2017-07-01
---
Cron jobs can be easily removed simply by providing a wrong options. I usually use the command 'crontab -e' to add/modify all my scheduled cron jobs. (In fact, I just mistyped e as r haha) Sometimes, I mistyped to option 'r' instead of 'e' which in fact will removed all my cron jobs according to [this](https://www.computerhope.com/unix/ucrontab.htm). When the moment I first did it, I panicked. Searched online and was trying to figure out how to recover this. Then, I got this idea of creating a bash script/command line tool that will help others to recover from disaster. And, here is what I [did](https://github.com/poanchen/recover-crontab).

Say, one day you accidentally did this. You do not need to panicked because you got me. I will walk you through how to use this script to recover all your deleted cron jobs.

First step, you need to download the latest released version of the bash script from my [GitHub repo](https://github.com/poanchen/recover-crontab/releases).

<pre>
  <code class="bash">
    wget https://github.com/poanchen/recover-crontab/archive/x.x.x.zip
    wget https://github.com/poanchen/recover-crontab/archive/x.x.x.tar.gz
  </code>
</pre>

Unzip them,

<pre>
  <code class="bash">
    unzip x.x.x.zip
    tar xvzf x.x.x.tar.gz
  </code>
</pre>

Go to the directory and run the script like this,

<pre>
  <code class="bash">
    ./recover-crontab.sh -u [PUT YOUR USERNAME HERE]
  </code>
</pre>

You will be promoted to input your scheduled time like this,

<img src="https://raw.githubusercontent.com/poanchen/recover-crontab/master/demo.PNG" alt="recover-crontab demo"><br>

At the end, you can find the ready-to-go command from the stdout or output.txt file. Hint: Use command 'crontab -e' to add/modify your cron jobs.

## Wrapping Up

Hopefully this guide has help you to recover from the incident. Thank you for reading! 

## Resources

I'll try to keep this list current and up to date. If you know of a great resource you'd like to share or notice a broken link, please [get in touch](https://github.com/poanchen).

### Getting started

* [recover-crontab](https://github.com/poanchen/recover-crontab) by [PoAn (Baron) Chen](https://www.github.com/poanchen)
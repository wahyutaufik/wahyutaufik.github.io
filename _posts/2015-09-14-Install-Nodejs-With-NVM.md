---
layout: post
title: How To Install Node.js with NVM (Node Version Manager)
---

Introduction
============
If you already know what Node.js is what it's for and why it's cool, then skip straight to the installation directions. If you want to know a bit more about node and it's ecosystem read on.

For those who haven't heard node.js is, it is the hot new cool kid on the block in web application development. It lets you write web apps that use Javascript on both the server and the client, so you don't need to know multiple programming languages to program your website. It's also really good at handling real-time concurrent web applications, which makes it a great choice for a lot of modern web apps.

The downside though is that all these cool new features are really, really new. As a result, getting up and running with node.js isn't as easy as, say, getting WordPress up and running on your web server.

This is the first in a series of how to install, code in, and use node. Joyent, the team behind node.js, has been improving node.js at a frantic pace, to the point where there are multiple releases of the software every month. For the most part, they've done a pretty good job of keeping things compatible; the things you write for one version of node will work just as well in the next. But nonetheless, sometimes a particular node app will only work with one version of node. And you will need to upgrade or downgrade your node.js install in order to use it.

This used to be a pain, but the node community has come together and created a great solution that lets you easily manage all your node installations and change node versions whenever you feel like it. It's called NVM, or the Node Version Manager.

Installing Node.js
==================
The install process couldn't be easier. Once you're logged into your VPS, run this command:

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.26.1/install.sh | bash
```

or Wget:

```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.26.1/install.sh | bash
```

You'll see some output fly by, and then nvm will be installed. You will see a line that says:

=> Close and reopen your terminal to start using NVM

It's not actually necessary to log out, we just need to make sure that the changes nvm made to your path are actually reflected, so just do:

```
source ~/.profile
```

Alternatively, run the command suggested in the output of the script. Now type:

```
nvm ls-remote
```
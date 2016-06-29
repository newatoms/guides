> **Goal of this guide:** Show you how you can run a local server using firebase serve

# How to run a local server using firebase serve

When creating websites you need to see what your new implementation looks like before displaying it online. No good having your visitors see all your trial and errors, is it ;)

One way to avoid this is by 'running a server' locally. You can change whatever you like and you'll be the only person who'll see it––except for maybe your colleague who'll be amazed by your inclusion of a purple horse on your website!

## If you've run a local server before

> Skip this bit if this is your first time running a local server

1. [Navigate in the terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html) to the folder of the website you want to change.
2. run ```firebase serve```
3. open a browser and go to the localhost address that is displayed in the terminal.

## It's not that techy!

What we'll be dealing with:
* [Npm](https://www.npmjs.com/), which enables you to easily make use of the awesome scripts that others wrote.
* [Node](https://nodejs.org/en/), enables you to use [javascript](http://www.w3schools.com/js/default.asp) code in a non-[browser](https://googleblog.blogspot.nl/2009/10/what-is-browser.html) setting.
* [Firebase](https://firebase.google.com/) is a product that offers, among others, a database and hosting.
* [The Mac terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html), read this guide if you don't know how to navigate through folder using the terminal.

## Installing

This is a bit of a boring process but only needs to be done once per computer.

1. Download and install [Node](https://nodejs.org/en/)
2. Open your terminal ```cmd-space -> terminal```
3. Run ```npm install firebase tools -g``` *[click here](/how-to-solve-mac-permission-errors) if you get an error*
5. Follow the steps described in ```If you've run a local server before```

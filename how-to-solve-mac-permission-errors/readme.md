> **Goal of this guide:** To help you solve the annoying permissions error that the mac sometimes gives when installing something via the terminal

# How to solve the permissions error

When installing software via the [Mac terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html) you might can the error: ```Error: EACCES ...```. If you're installing something outside of the terminal, you'll usually see a popup.
This happens because some Macs are protected, by default, against programs overwriting certain files. Unfortunately the Mac might be overprotective in some cases.

If you got the error by installing via NPM [use this guide](https://docs.npmjs.com/getting-started/fixing-npm-permissions).
Otherwise use [this guide](http://www.macworld.com/article/2911697/the-ins-and-outs-of-an-os-x-permissions-fix.html)

### When the guides don't offer a solution

If those guides did not solve the problem there is a last resort (not adviced, but solves the problem if you're really stuck).
You can go, in the [terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html) , to the folder/file mentioned in the error and execute.

`sudo chmod 777 filename`

Where you replace ```filename``` with the file name and extension that gives you the permission error. This is not recommended though since it might mean you open up the file to be accidentally overwritten while it might be important for your system to work with, so ask someone for some help or Google it.
[Here's a guide with more information on the chmod trick](http://www.chriswrites.com/how-to-change-file-permissions-using-the-terminal/)
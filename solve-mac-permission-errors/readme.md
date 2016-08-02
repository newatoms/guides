> **Goal of this guide:** To help you solve the annoying permissions error the Mac Terminal sometimes returns when installing something

# How to solve permission errors

When installing software via the [Mac Terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html) you might get the error: ```Error: EACCES ...```. If you're installing something outside of the Terminal, you'll usually see a popup.
This happens because some Macs are protected, by default, against programs overwriting certain files. Unfortunately the Mac might be overprotective in some cases.

If you got the error by installing via NPM [use this guide](https://docs.npmjs.com/getting-started/fixing-npm-permissions).
Otherwise use [this guide](http://www.macworld.com/article/2911697/the-ins-and-outs-of-an-os-x-permissions-fix.html)

### When the guides don't offer a solution

If those guides did not solve the problem there is a last resort (not adviced, but solves the problem if you're really stuck).
You can go, in the [terminal](http://www.macworld.com/article/2042378/master-the-command-line-navigating-files-and-folders.html) , to the folder/file mentioned in the error and execute.

`sudo chmod 777 filename`

Here you replace ```filename``` with the file name and extension that got you the permission error. This method is not recommended though. The file can actually be important to your system and it might get overwritten on accident! Rather ask someone for some help or Google it.
[Here's a guide with more information on the chmod trick](http://www.chriswrites.com/how-to-change-file-permissions-using-the-terminal/)

# How to make a guide

To create an understandable guide make sure you keep the following points in mind.
* Never assume the reader understands the terminology you use, so always provide a explanation or a link explaining what you mean.
* Always make clear what the reader can expect to learn from a guide at the beginning of the guide to avoid being disappointed halfway trough.
* People should be able to search for a specific topic in your guide, so make sure you clearly separate different chapters and topics in you guide.

## Adding your guide to the guides

To add a guide complete the following steps
* Create a new folder within guides a name it [guide-name] replace all " " with "-"
* Copy your guide to `guides/[guide-name]/` and change the name to `readme.md`. This enables the visitor to instantly view your guide when they are in the folder of your guide on github.
* If there are local images in your guide you can store them in `guides/images/[your-image.filetype]`
* The path to your images is `../images/[your-image.filetype]`
* Add the guide to this readme.md on the bottom of the "List of all guides" lists in the following way:

```
  |[name-guide](folder-name-guide)|[goal of the guide]
```
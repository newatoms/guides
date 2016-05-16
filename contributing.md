# How to make a guide

To create an understandable guide make sure you keep the following points in mind:
* Never assume the reader understands the terminology you use; always provide a explanation or a link explaining what you mean.
* Always make clear what the reader can expect to learn from a guide at the beginning of the guide to avoid disappointment halfway trough.
* People should be able to search for a specific topic in your guide, so make sure you clearly separate different chapters and topics.

## Adding your guide to the guides

To add a guide complete the following steps:
* The title of a guide should always start with 'How to'
* Create a new folder within *Guides* and name it [guide-name]. Replace all " " with "-".
* Copy your guide to `guides/[guide-name]/` and change the name to `readme.md`. This enables the visitor to instantly view your guide when they are in the folder of your guide on github.
* If there are local images in your guide you can store them in `guides/images/[your-image.filetype]`
* The path to your images is `../images/[your-image.filetype]`
* Add the guide to this readme.md on the bottom of the "List of all guides" in the following way:

```
  |[name-guide](folder-name-guide)|[goal of the guide]
```

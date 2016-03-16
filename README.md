# Guides

Hia👋! Welcome to the New Atoms Guides. We write these guides on how to do all the things we do. These serve to teach people interested in our ways but also to reassure.

Here you can find guides on used tools, communication, workflows, rules and most important, how to make awesome things. It's part of every team members job to edit the guides in order to share what we learn.

## All of the guides

Here you find a list with links to all guides and their goal.

|How to … |Goal of the guide              |
|--------|-----------------------------|
|[use text-editor Atom](atom-guide)| Helping you to use Atom, a text editor we use in combination with github |
|[use the Achievable board](board-guide) | Explaining how we work with our workflow board and optimizing the use of it  |
|[create awesome content](board-guide)| Helping you make the most awesome content you can make|
|[use GitHub](github-guide) | Guide on how to build documents and websites with the service called Github |
|[publish to Medium](medium-guide)| Helping you use Medium |
|[use Slack for team communciation](slack-guide) | Helping you use our main communications tool, slack.
|[communicate as content.supply](communication-guide) | Helping to communicate with the outside world
|[prepare for an interview](interview-guide) | Helping to prepare for an Interview |
|[use Polymer databinding](databinding) | How to communicate between elements using databinding in Polymer |
|[create a Polymer element](creating-elements) | Understanding the core concepts of coding in Polymer |
|[solve Polymer errors](fixing-errors) | Create a understanding of debugging web-apps |
|[turn a pitch into a blog post](turn-a-pitch-into-a-publishable-blog-post)| help you to create and work on a user story for a blog post |
|[scrape information from LinkedIn](web-scraping) | Extract data from LinkedIn profiles into a structured json format |
|[be a Managing Director](be-a-managing-director) | Explaining what it means to be a managing director |

Use the [Glossary](glossary) to find definitions of words we use and how we use them.

## How to make a guide

To create an understandable guide make sure you keep the following points in mind.
* Never assume the reader understands the terminology you use, so always provide a explanation or a link explaining what you mean.
* Always make clear what the reader can expect to learn from a guide at the beginning of the guide to avoid being disappointed halfway trough.
* People should be able to search for a specific topic in your guide, so make sure you clearly separate different chapters and topics in you guide.

## How to add a guide

To add a guide complete the following steps
* Create a new folder within guides a name it [guide-name] replace all " " with "-"
* Copy your guide to `guides/[guide-name]/` and change the name to `readme.md`. This enables the visitor to instantly view your guide when they are in the folder of your guide on github.
* If there are local images in your guide you can store them in `guides/images/[your-image.filetype]`
* The path to your images is `../images/[your-image.filetype]`
* Add the guide to this readme.md on the bottom of the "List of all guides" lists in the following way:    

```
  |[name-guide](folder-name-guide)|[goal of the guide]
```

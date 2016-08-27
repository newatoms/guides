> Goal: To serve as a style guide for writing markup, code and styles at New Atoms

# How to style your files

We want the way that we write JavaScript, HTML, MarkDown CSS and other programming or markup languages to be written in a similar style to make them easier to read and prevent difficult but useless merge conflicts.

Because we want to create re-usable code which is understandable by others that might not be particularly acquainted with it’s syntax, we rely heavily on [comments](https://en.wikipedia.org/wiki/Comment_(computer_programming)) and [Javadoc/DocBlocks](https://en.wikipedia.org/wiki/Javadoc). These enable us to clearly document what happens and how others can re-use our code.

## The separation of concerns

To everything we produce there are three distinct things we need to communicate to machines in order to visualise what we want. 

- Markup: The content of what we’re trying to say in a structure that makes sense
- Style: How the browser (or printer) needs to visually display what we’ve made
- Logic: How what we’ve made should adapt to interaction and the world around it

These are separated because they need different mental models to think about them, additionally it makes it easy to find where something is.

The separation is successful when we can change the markup without changing the style, the style without changing the logic etcetera.

## Markup: Structure

The Markup is where we define the content of what we make. This is the place where we put all of the elements of our creative work and define what their relationships are to each other.

Although it is often possible to use certain visual elements in markup, you shouldn’t. It should be specified in the design what emphasis and similar contexts should look like. A famous difficult one is the _line break_, signified as `<br>` in HTML and as two spaces `  ` at the end of a line in MarkDown, since this often is not used for context but for design making it hard to design well without changing the HTML again.

### HTML

By far the most common Markup language, mostly because it is the core building block of the web. Every webbrowser in the world understands HTML, even those that do not have a screen/are audio only, or are run by computers.

Try to write one tag per line for clarity.

You can use CSS, JavaScript and SVG in your HTML.

### SVG

This is an interesting one, as it is a medium for making drawings, so one would easily assume this would be design. A good SVG uses a HTML like markup to clarify its contents (e.g. the drawing) and uses CSS for styling things that are in the realm of design, making it easy to adapt for differing designs.

Example: You have a drawing of a man in a shirt that has the primary colour of the website. The drawing of the man is the contents, so you shouldn’t necessarily need to be able to change that, but the colour of it’s shirt needs to changeable.

You can use HTML, CSS and JavaScript in your SVG.

### (GitHub Flavored) MarkDown

[MarkDown](https://daringfireball.net/projects/markdown/) is a markup language that is a subset of what is possible with HTML and a different notation. MarkDown focusses on readability and ease of writing, and is used a lot for blogging, simple text editing and the `readme.md` files of GitHub.

MarkDown is easy to read and fast to use. To learn it effectively requires some learning as many of the tokens are hard to distinguish like the `  ⏎` for a linebreak.

We usually write in a specific superset of Markdown called [_GitHub Flavored MarkDown_](https://guides.github.com/features/mastering-markdown/) which adds some niceness such as the ability to [create task lists, tables and use Syntax highlighting for code examples](https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown).

You can use HTML and SVG in your MarkDown.

## Logic: Code

All of the interactivity and everything that changes in a creative work is driven by the underlying logic, expressed in code.

### JavaScript

We use JavaScript because nigh every browser supports it and we can also write server side (NodeJS) applications in it.

If we’re writing JavaScript we try to stick to [StandardJS](http://standardjs.com/rules.html) as much as possible. It calls for clean code with easy to understand constructs.

## Style: Visual presentation

The style dictates the whole presentation, from fonts, to margins to how things are positioned on a page.

### CSS

Famously hard to understand, and hard to understand the effects of changing things, CSS might be one of the best reasons to use Polymer and it’s ability to scope CSS to only a specific part of the code.

We prefer using FlexBox over the BoxModel because it is generally easier to understand and more flexible.

An amazing example of how you can make great designs regardless of the markup is at [CSS Zen Garden](http://www.csszengarden.com/), which features over 200 designs for the same page.

## Components for the web and severs

In order to make make the things we develop re-usable and easy to understand we develop _components_.

### Polymer Elements

[Polymer Elements](https://www.polymer-project.org/1.0/) are additions to the built in HTML vocabulary of the browser that you can use to create encapsulated mini-applications that have their own markup, logic and style and that are independent from other elements.

Polymer Elements take the philosophies behind how the browser works a step further and make it easy to develop in a non-linear fashion.

For the design and documentation of Polymer Elements, please refer to the [Polymer Style Guide](polymerelements.github.io/style-guide).

### Docker / Heroku workers

Workers are programmes that run continually on servers responding to events in the outside world.

These are preferably written in JavaScript and run on NodeJS.

## General file formatting

To prevent merge conflicts and make the code uniformly easy to read we have a few standars that we employ:

- Indentation: 2 spaces
- Newlines: Not more than 2 empty for visual function

### How to use [JS-beautify](https://github.com/beautify-web/js-beautify) to automatically format your files

JS-beautify can be installed in your text editor or on your command line to automatically format your files, unify indentation and similar fixes.

An example `.jsbeautifyrc` file:

```json
{
  "_default": {
    "indent_size": 2,
    "indent_char": " ",
    "indent_with_tabs": false,
    "max_preserve_newlines": 2,
    "preserve_newlines": true,
    "brace_style": "collapse",
  },
  "html": {
    "indent_inner_html": true
  }
}
```


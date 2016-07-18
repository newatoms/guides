> If someone with a basic understanding of HTML, CSS and JavaScript reads this guide, they will understand what Polymer is and how it can be used.

# How to start using [Polymer](../glossary/polymer.md)

Polymer enables us to create our own [elements](../glossary/element.md), standardised building blocks that are easily maintained, combined into an application and reconfigured into other applications.

## The idea of custom elements

You see a lot of the same functionality, content or design multiple times on a site and/or on multiple sites. For example text inputs, user login forms, navigation, tooltips, icons etcetera. Custom elements enable us to make these things into packages that can be used multiple times and on multiple websites.

As an example: you would like to create a counter that will show everyone on your website how many visitors you've had since the nineties started. Using Polymer we can make a `<my-counter>` element with all of its HTML, CSS and JavaScript embedded in it. This way we can easily use it on every one of our websites.

The idea💡 is that you write elements that are custom made for one goal. They should be able to perform only the single task that will result in obtaining their goal. However, you should be able to reach this goal each time you use the element. Your code, therefore, should never include details that are only valid for the current project.

> There is one exception to the "don't write code that is only valid for the current project" rule. Since the entire site is built with elements, some elements will have to be project-specific. Try to limit using them as much as possible, though!

Elements can receive input arguments that change how the element behaves. For example, a text input can be told that only dates are valid input options. You could write a `text-date-input` element, but sometimes functionalities are so similar that you want them to be in the same element to make it easier to maintain them.

It's difficult to define precisely what the goal of the element is and how this goal can be reached using values that might differ over different parts of the site/ different sites. Take your time 🕚 and [Read our guide on how to create a new element](../creating-elements/readme.md).

## Communication between elements

Polymer Elements can communicate with each other.🗣 An element that is called inside another element is called a 'child'; and the element an element is inside of is the 'parent'. 

Elements can communicate in different ways. 
- [Two way data binding](../databinding/readme.md) between elements, and
- [Events](https://www.polymer-project.org/1.0/docs/devguide/events.html): you can let polymer fire an event when something happens, e.g. a user presses a button. The event contains information of the event itself and information you send with it (array, object, string, etc.).

## There are three distinct 'languages' in Polymer

A polymer element consists of three languages: [HTML](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction), [CSS](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started) and [JavaScript](https://developer.mozilla.org/en-US/Learn/JavaScript).

HTML is for structure/content, CSS for styling/design and JavaScript for logic/interaction. Each of these is it's own language. 

In an element we first define our CSS between the `<style>` HTML tags, then the HTML contents of this element's template and the JavaScript logic at the end between the `<script>` tag.

> Note that some standard implementations of html/css/javascript are not valid in Polymer ❗️ This makes finding (valid) help online somewhat more difficult. Polymer has been updated as well, rendering some answers to earlier questions false 🚫. Use the filter date function on Google to limit search results to after june 2015.

## So now what...?

There are [plenty of other guides](../README.md) on Polymer, which will give you the information you need to start implementing something. Since we're using [Git](../glossary/git.md), you can't really destroy anything except for the database. Please don't do that 😬. See our [create a new element guide](../creating-elements/readme.md) on how to avoid this.

Ask a team member if you're stuck or if you're afraid you'd break 🔥 something. Good luck! 😉

## Using elements created by others

With Polymer we can make elements that can be used by everyone. And we can use elements shared by others. For example: we rely heavily on elements made by the Google Polymer team.

You can find custom elements made by others:

- [Polymer elements](https://elements.polymer-project.org/) is a collection of very useful elements that have been written by Google. They are free to use and very awesome. You will probably not be able to write better code than what is inside those elements so if you can make use of them, do it.
- [Customelements.io](https://customelements.io/) is a website where people share their elements. The quality differs but the popular ones can be quite useful (note that outdated elements stay on the site 😞).

Read the documentation and the code of the element that you're using. Most of the time investing in a better understanding of the functionalities of the element will help you solve your problem.

## Helpful links

You can find a lot of help online. Do note that Polymer is relatively new and that most of the documentation has been written by, and for, programmers. Initially finding answers to your questions might be a bit frustrating but Polymer is so awesome that this initial phase is more than worth it.

[StackOverflow Polymer](https://stackoverflow.com/questions/tagged/polymer) is a community where people ask and answer each other's Polymer related questions.

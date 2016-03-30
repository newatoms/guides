# How to start using Polymer

### The idea of elements

A lot of the same functionalities can be found on different sites and even within the same site. Think of text-input boxes, user log-ins, keeping track of user behavior, etc.. It would be very useful if for each site you build you could quickly reuse the already written functionality. Polymer allows you to do exactly this. An entire site is comprised solely of elements⚛.

The idea 💡is that you write elements that are custom made for one goal. They should be able to perform only the single task that will result in obtaining their goal. However, you should be able to reach this goal each time you use the element. Your code therefore should never include details that are only valid for the current project.

> There is one exception to the "don't write code that is only valid for the current project" rule. Since the entire site is built with elements, some elements will have to be project specific (try to limit using them as much as possible though!).

Elements should however be able to receive input arguments that might alter the function of the element. For example, a text input element can be told that only dates are valid input options. You could write a text-data-input element but sometimes functionalities are so similar that you want them to be in the same element.

It's difficult to define precisely what goal of the element is and how this goal can be reached using values that might differ over different parts of the site/ different sites. Take your time 🕒 [Read our guide on how to create a new element](https://github.com/newatoms/newatoms/blob/ready/internal/guides/how-to-create-a-new-element.md)

### Communication between elements

Elements communicate with each other.🗣 An element that is called inside another element is called a 'child', the calling element is called the 'parent'.
These elements can communicate via different ways. One way is databinding between elements -- see our guide 'How to use data-binding' [here](../databinding/readme.md).

Another way of communication between elements is [events](https://www.polymer-project.org/1.0/docs/devguide/events.html). You can let polymer fire an event when something happens, e.g. a user presses a button. The event contains information of the event itself and information you send with it (array, object, string, etc.).

### There are three distinct 'languages' in Polymer

A polymer element consists of three languages: [html](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Introduction), [css](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started) and [javascript](https://developer.mozilla.org/en-US/Learn/JavaScript).  
HTML is for structure, css is for styling and javascript is for logic. Each one has it's own language and rules. The order we use is first css, than html and js at the end. ```<Style>``` indicates CSS and ```<script>``` is javascript.
> Note that some standard implementations of html/css/javascript are not valid in Polymer ❗️ This makes finding (valid) help online somewhat more difficult. Polymer has been updated as well, rendering some answers to earlier questions false 🚫. Use the filter date function on Google to limit search results to +-4 months.

### So now what...?

Read all our other [guides on Polymer]((https://github.com/newatoms/guides)) and start implementing something. Since we're using Git you can't really destroy anything except for the database. Please don't do that 😬. See our [create a new element guide](https://github.com/newatoms/newatoms/blob/ready/internal/guides/how-to-create-a-new-element.md) on how to avoid this. Ask a team member if you're stuck or if you're afraid you'd break 🔥 something. Good luck! 😉

### Helpful links

Besides the [guides](https://github.com/newatoms/guides) we wrote ourselves you can find a lot of help online. Do note that Polymer is relatively new and that most of the documentation has been written by, and for, programmers. Initially finding answers to you questions might be a bit frustrating but Polymer is so awesome that this initial phase is more than worth it.
- [Polymer on Stackoverflow](https://stackoverflow.com/questions/tagged/polymer) is a place where people ask and answer each others Polymer related questions
- [Polymer elements](https://elements.polymer-project.org/) is collection of very useful elements that have been written by Google. They are free to use and very awesome. You will probably not be able to write better code than what is inside those elements so if you can make use of them, do it.
- [Customelements.io](https://customelements.io/) is a website where people share their elements. The quality differs but the popular ones can be quite useful. (note that outdated elements stay on the site 😞)
- Read the documentation and the code of the element that you're using. Most of the time investing in a better understanding of the functionalities of the element will help you solve your problem.
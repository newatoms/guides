> **The goal of this guide:** Understanding the core concepts of creating elements.

# How to create a [Polymer](https://github.com/newatoms/guides/blob/ready/glossary/polymer.md) element

A Polymer element is a custom [HTML element](http://www.w3schools.com/html/html_elements.asp). It can be used like other HTML Elements in your websites with the addition of some nice extra magics.

An element should fulfill one function and should be reusable in multiple contexts. For instance: we use the `<user-chip>` element everywhere where we are mentioning a user in the Interface. If we want to display our users in a different way, we only have to update one file.

## 1. Check if there is an element you can reuse

Is there an element on the site that has a similar functionality? Can you solve the [achievable](../glossary/achievable.md) by expanding the functionality of this element?

For example: the [paper-input element](https://elements.polymer-project.org/elements/paper-input) is not limited to plain text but can take an argument to restrict the user input to a social security number. Only do this when it clearly makes sense though!

[The Polymer catalog 💕](https://elements.polymer-project.org/) has a lot of very good elements you can use for free.
[Customelements.io](https://customelements.io) is also growing quite fast. It's a site where people contribute their code, mostly open source. Not all code is great, but a lot of it is. Also, not all code is Polymer code.

## 2. Close your laptop!

Never start writing code right away ⏳. If an [achievable](../glossary/achievable.md) requires you to make a new element, take a deep breath and close your laptop.

Think about what the function of the element is. Spend some time on it. Imagine future scenarios where the element can be used 🔮. Pinpoint what the element should do, and think carefully about what it shouldn't do.

You are likely to think about building functionality that actually falls outside the scope of a good element. Don't build the element only for the achievable you are working on though, think bigger and make something reusable.🚀

## 3. Create a new element

So you need to build a new element. Think about which other elements the new element should interact with. What information does the new element need from them and what can it give back? 🗣

Create an HTML file with a name that describes the the element very well and at least one `-`, or hyphen, in it, for instance `user-chip`, `project-name`, `user-login-form` or `helicopter-landing-pad`.

To get started you could copy and paste the content of [`seed-element`](https://github.com/newatoms/interface/tree/ready/web/_components/seed-element) into your empty file to setup your new element.

Every element should be able to work in isolation and you should build/test it in isolation. Create a demo file, insert your element, give it the relevant data and test your file. And don't forget to document your element well, examples of this can all be found in the `seed-element`.

Start with a small implementation and test it.🔬

Continue by writing and testing another implementation. Continue until the entire element is built. When it works on its own, try to implement it in other (relevant) elements wherever it can improve the code-base.

For more on how to make an element, read the [element style guide](https://github.com/newatoms/interface/blob/ready/docs/style-guide.md).

## Elements that communicate with the database

If your element needs to communicate with Firebase then [Double Dutch](http://nl.urbandictionary.com/define.php?term=double+dutch)🛡:

* Make a backup of the [database](https://interface.firebaseio.com)! (export data -> in the browser)
* Use the [playground database](https://interface-playground.firebaseio.com ) and never the live database! (import the newest database if needed using the Firebase interface in the browser)

## Ask for help

If you come across terms you don't understand you can:

* Google them
* Ask a team member within digital reach
* File issues in the relevant repos on [GitHub](https://github.com/polymerelements/)
* Ask questions on [Stack Overflow](http://stackoverflow.com/questions/tagged/polymer).

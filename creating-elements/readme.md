> **The goal of this guide:** Understanding the core concepts of creating elements.

# How to create a Polymer element

A Polymer element is a custom [HTML element](http://www.w3schools.com/html/html_elements.asp), it can be used like other HTML Elements in your websites with the addition of some nice extra magics.

An element should fulfil one function and should be reusable in multiple contexts. For instance if we use the `<user-chip>` element everywhere where we are mentioning a user in the Interface we only have to update one thing is something changes in the way we want to display users.

## 1. Check if there is an element you can use for this already

Is there an element on the site that has a similar functionality? Can you solve the user story/bugreport by expanding the functionality of this element?
For example the [paper-input element](https://elements.polymer-project.org/elements/paper-input) is not limited to plain text but can take an argument to restrict the user input to a social security number. Only do this when the it clearly makes sense though!

[The Polymer catalog 💕](https://elements.polymer-project.org/) has a lot of very good elements you can use for free.
[Customelements.io](https://customelements.io) is also growing quite fast. It's a site where people contribute their code, mostly open source. Not all code is great, but a lot of it is. Also, not all code is Polymer code.

## 2. Close your laptop!

Never start writing code right away ⏳. If an [achievable](../glossary/achievable.md) requires you to make a new element, take a deep breath and close your laptop. 

Think about what the function of the element is. Spend some time on it. Imagine future scenarios where the element can be used 🔮. Pinpoint what the element should do, and think carefully about what it shouldn't do.

You are likely to think about building functionality that actually falls outside the scope of a good element. Don't build the element only for the achievable you are working on though, think bigger and make something reusable.🚀


All elements should be able to function on their own. If you need data from the outside, give the data in the demo.
**Build elements in isolation!**

## Elements that communicate with the database

If your element needs to communicate with Firebase then [Double Dutch](http://nl.urbandictionary.com/define.php?term=double+dutch)🛡:
* Make a backup of the [database](https://interface.firebaseio.com)! (export data -> in the browser)
* Use the [playground database](https://interface-playground.firebaseio.com ) and never the live database! (import the newest database if needed -> in the browser)

## Implementations

This entirely depends on your type of element. A few tips:
* Import other elements (top of the page)
* Keep the format of your element according to [our rules](https://github.com/newatoms/interface/blob/ready/docs/style-guide.md).
* Make sure everything closes correctly: e.g. forgetting to close a template will destroy your element.🔥
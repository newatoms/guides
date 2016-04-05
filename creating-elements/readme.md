> **The goal of this guide:** Understanding the core concepts of creating elements.

# How to create a Polymer element

A Polymer element is a custom [HTML element](http://www.w3schools.com/html/html_elements.asp), it can be used like other HTML Elements in your websites with the addition of some nice extra magics.

An element should fulfil one function and should be reusable in multiple contexts. For instance if we use the `<user-chip>` element everywhere where we are mentioning a user in the Interface we only have to update one thing is something changes in the way we want to display users.

## 1. Check if there is an element you can use for this already

Is there an element on the site that has a similar functionality? Can you solve the user story/bugreport by expanding the functionality of this element?
For example the [paper-input element](https://elements.polymer-project.org/elements/paper-input) is not limited to plain text but can take an argument to restrict the user input to a social security number. Only do this when the it clearly makes sense though!

[The Polymer catalog 💕](https://elements.polymer-project.org/) has a lot of very good elements you can use for free.
[Customelements.io](https://customelements.io) is also growing quite fast. It's a site where people contribute their code, mostly open source. Not all code is great, but a lot of it is. Also, not all code is Polymer code.

## Create a new element

So you need to build a new element. Think about with which other elements the new element should interact. What information does the new element need from them and what can it give back? 🗣

Create a html file with a name that describes the functionality of the element very well. The name of the file has to have a hyphen - in it. Copy paste the content of seed-element.html into your empty file to setup your new element.
Create a element-name.html file in the demo folder and test your file.

> You can go to localhost:x000/_components/element-folder/demo/element-name.html to test your element
(e.g. http://localhost:3000/_components/doable-item/demo/doable-detail.html).

Remove all redundant code from your element and replace seed-element with element-name. Start with a small implementation and test it.🔬
Does it work? Great, write documentation for it (see seed-element.html on how to do this).
Continue by writing and testing another implementation. Continue until the entire element is built. When it works on it's own, try to implement it in other (relevant) elements.

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
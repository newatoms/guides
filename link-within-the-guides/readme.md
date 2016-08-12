> **The Goal of this guide**: showing you how to link between guides and glossary items on the guides [repository](../glossary/repository.md).

# How to link within the guides

For our guides repository we create relative links when we want to link to other guides or glossary items.

For example if you're working on a guide and you are talking about an *achievable* the syntax goes like this:

1. You go back one folder with `../`
* then you go to the glossary folder `../glossary`
* finally you go to the achievable file `../glossary/achievable.md`

In [markdown](../glossary/markdown.md) it looks like this:

`[Achievables](../glossary/achievable.md)`

We don't use absolute linking:

`[Achievables](https://github.com/newatoms/guides/blob/ready/glossary/achievable.md)`

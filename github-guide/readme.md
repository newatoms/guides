> The goal of this guide: To help you get started on using our version control tool: Github.

<img src="../images/github-mark.png" width="100">

# How to use GitHub

[Github](http://github.com/) is a tool that we use for the creation of all our content and code. In the core it is comparable with how you can work on one Google document with multiple people through suggesting changes. Github works on the same principle but way better, cooler and safer.

Github is a tool that enables the users to very safely improve things that are created in small comprehensive steps that get reviewed by other users. This way everyone can freely contribute to what you are building without the fear of changing something permanently. It is mainly designed with the idea that nothing great was ever made by one person, and that the easier and safer it feels to improve something, the better it is what was created.

In opposition to the system used by things like Google Docs and Microsoft Word, GitHub works with a version control system based on commits and branching. This means every collaborator has a own version – or branch – they work on. This branch is later explicitly merged with branch that all collaborators are starting from. All content on this branch has been reviewed and tested, and should therefore work well. Every change is added to a branch with a commit in which the contributor explains what he/she has added, and why, in a short message.

The explicit merging of your contributions with those of others allows for a set moment for contributors and automated software to review the things that have changed.

Github has quite a steep learning curve, but once you go Github you'll never want anything different.

## How we use Github

We work with multiple repositories (i.e repos). You can see this [New Atoms repository page](https://github.com/newatoms) as a hard drive containing all projects or products. For example: right now you are reading *the github guide* in the *guides* repo. *Guides* is a product of New Atoms, just like *content.supply* or *editorial.supply*.

Always read the readme.md file that is opened automatically if you enter a repo.

All our research is stored within the designated project or product repos like pitches, posts and research, insights, private and internal (i.e. market research, customer acquisition, pitch decks etc.). Folders with a lower dash before the folder name in repositories are not rendered on websites, but they're still viewable by anyone who can access the repo. We also store a lot of our sites (like the interface) in the repositories (e.g. html, layout etc.).

### Github hierarchy

Github works with branches. We work with the following hierarchy:

* The *live* branch: The content of these branches is 'live' and always works. For example, the website (if any) is rendered from files from this branch.
* The *ready* branch: This is a copy of the *live* branch. Here, documents should be fit to print and *merge-able* with the *live* branch. It is a last check before we push the content to the 'live' branch. We explain *merging* later on. From the *ready* branch you create a new branch and give it a selfexplanory name.

> You will sometimes see a *gh-pages* branch instead of a live branch. The product of that repo is than hosted by [Github pages](https://pages.github.com/).

### Creating a file or editing a lot in one file

1. Go to the file you want to edit or go to the folder where you want to create a new file.
2. Make a branch and give it a self explanatory name.
3. Make a new file in designated folder (filename + filetype, for text it's *.md* for *[Markdown](../glossary/markdown.md)*).
4. When writing or editing keep in mind to make commits (i.e. saves or changes) when changing something.
5. Each change you make requires a commit -- if you edit an existing document you have to commit at least once per sentence, if you create a new document you can commit each paragraph. This allows you and others to accept or reject each individual change and enables you to explain why you made a certain change.

Example: ```internal/guides/medium-guide```

---

**1:** <img src="../images/branching-1.png" width="250">

---


**2:**<img src="../images/create-branch.png" width="250">

---

**3:** <img src="../images/edit-file.png" width="250"> **4:**<img src="../images/commit.png" width="350">

---

**5:** <img src="../images/see-commit.png" width="250">

---

### The Pull request

If you're happy with all your changes in your new file, you have to make a *pull request* and add the url of your pull request––which you can find in the address bar of you browser––to the achievable you just finished. Now your changes will be reviewed by somebody else who will either comment, add commits (changes) or merge the request (this means the file is good to go).

---

**1:**<img src="../images/pull-request.png" width="300">

---

**2:** <img src="../images/pull-request-button.png" width="200">

---

**3:**<img src="../images/right-branch.png" width="600">

---

**4:**<img src="../images/name-branch.png" width="400">

---

You created a create pull request! Congratulations! Every time it feels great.

If somebody comments the original owner and everybody who has commented/committed to the pull request will receive a notification.

> You can choose not to receive messages in the Github settings

### A shortcut when changing something small

When changing something small, you can go to the designated file and hit the edit icon. Do not commit directly on the ready branch, because that would be "illegal", but choose the option to *'Create a new branch for this commit and start a pull request'*.


### Discuss and Merge

<img src="https://media.giphy.com/media/kFJ7NdGw4A4o0/giphy.gif" width="100%">

You can edit a pull request or comment on certain parts of the file by clicking the + sign on the left. When you click, your comment will be visible in the conversation menu.

When everyone is happy about the document and the file is fit to go to the ready branch, the person reviewing the pull request can push the big green merge button on the bottom of the conversations menu and press the delete branch button that appears after you have merged. Congratulations 🏅, The branch is *merged* with the ready branch and is fit to go live. High five 🙏!

## Working local on your own device

Working local means that you *clone* (i.e. copy) a repository from the Github client to your local device in your own designated folder.

You need to download [Github Desktop](https://desktop.github.com/) and a text editor, for example: [Atom](https://atom.io/). See also our [Atom guide](../atom-guide/readme.md) for further consult. A text editor comes in handy when writing a bunch of text.

[*Cloning a repository*](https://help.github.com/desktop/guides/contributing/cloning-a-repository-from-github-desktop/) means that you copy a repository from the browser on your device in your own folder architecture. You do this in your Github desktop application.

Make sure you select or create the right branch in the Github desktop.

> Never commit to the ready/live branch itself, unless you're fixing a breaking bug and you're 100% you don't break anything with the commit

Any change you'll make to a file in the folder (or subfolder) on your device results in a uncommitted change in github desktop. If you press commit changes, you in fact update your *local* branch. You now will have to publish your local branch in order share your changes with others. Press *sync*, if you want to push the local changes to an existing online branch with the same name or if you want to update your local branch with the content of the online branch.

So, there are two branches with the same name, one local and one online. Team members can't see your local changes and your local branch also doesn't automatically copy changes from the online branch. It takes an action from you to sync them.

Therefore, if you want to change or add a file you sync with the most recent branch on that repo that deals with the particular work you want to work on. This is often the branch *ready* if you create a new file and always the same as your local branch if it already exists.

### Add images

You can only locally add images by saving them in the designated folder (e.g. images-folder).

---

<img src="../images/right-branch-desktop.png" width="300">

---

Then, you can open the repository folder you want to work on in your text editor. The following image shows text editor Atom with on the left panel the local repository folder and on the right the preview window.

---

<img src="../images/atom-example.png" width="600">

---

## The dreaded merge conflict

If two people changed the same lines in the same file, or if one person decided to delete it while the other person decided to modify it, Git simply cannot know which change is correct. Git will therefore mark the file as having a conflict––which you'll have to solve before you can merge. Git will tell you which line resulted in a merge conflict. You have to decide, together with the other person who merged the file, which version is correct, or more common, create a new combined version.

> In [Atom](../atom-guide/readme.md) you have a [package](https://atom.io/packages/merge-conflicts) that will display <----READY and <----HEAD around the lines that resulted in the conflict.

See [Github's how to](https://help.github.com/articles/resolving-a-merge-conflict-from-the-command-line/), to deal with the merge conflict. Contact a team member in Slack if you're having problems solving the merge conflict.

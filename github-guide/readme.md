> The goal of this guide: To help you get started on using our version control tool: GitHub

<img src="../images/GitHub-mark.png" width="100">

# How to use GitHub

[GitHub](http://GitHub.com/) is a tool that we use for the creation of all our content and code. At its core, it is comparable with how you can work on one Google document with multiple people through suggesting changes. GitHub works on the same principle but better, cooler and safer.

GitHub is a tool that enables the users to very safely improve things in small, comprehensive steps that are then reviewed by other users. This way, everyone can freely contribute to what is being built without fear of changing something permanently. It is mainly designed with the idea that nothing great was ever made by one person, and that the easier and safer it feels to improve upon something, the better it will be.

In opposition to the system used by things like Google Docs and Microsoft Word, GitHub works with a version control system based on [commits](../glossary/commit.md) and [branching](../glossary/branch.md). This means every collaborator has her or his own version—or branch—they work on. This branch is later explicitly merged with branch from which all collaborators have started. All content on this branch has been reviewed and tested, and should therefore work well. Every change is added to a branch with a commit in which the contributor explains what he/she has added, and why, in a short message.

The explicit merging of your contributions with those of others allows for a set moment for contributors and automated software to review the things that have changed.

GitHub has quite a steep learning curve, but once you go GitHub you'll never want anything different.

## How we use GitHub

We work with multiple [repositories](../glossary/repository.md) (i.e repos). You can see this [New Atoms repository page](https://GitHub.com/newatoms) as a hard drive containing all milestones or products. For example: right now you are reading *the GitHub guide* in the *guides* repo. *Guides* is a product of New Atoms, just like *post.supply* or *editorial.supply*.

Always read the readme.md file that is opened automatically if you enter a repo.

All our research is stored within the designated milestone or product repos—pitches, posts and research, insights, private and internal (i.e. market research, customer acquisition, pitch decks etc.). Folders with a lower dash before the folder name in repositories are not rendered on websites, but they're still viewable by anyone who can access the repo. We also store a lot of our sites (like the interface) in the repositories (e.g. html, layout etc.).

### GitHub hierarchy

GitHub works with branches. We work with the following hierarchy:

* The `live` branch: The content of these branches is "live" and always works. For example, the website is rendered from files from this branch.
* The `ready` branch: This is a copy of the `live` branch. Here, documents should be fit to print and *merge-able* with the `live` branch. It is a last check before we push the content to the `live` branch (we explain *merging* later on). From the `ready` branch you create a new branch and give it a logical name.

> You will sometimes see a `gh-pages` branch instead of a live branch. The product of that repo is then hosted by [GitHub pages](https://pages.GitHub.com/).

### Creating a file or editing a lot in one file

1. Go to the file you want to edit or go to the folder where you want to create a new file.
2. Make a branch and give it a self-explanatory name.
3. Make a new file in designated folder (filename + filetype, for text it's *.md* for *[Markdown](../glossary/markdown.md)*).
4. When writing or editing, keep in mind to make lots of commits (i.e. saves or changes) when changing something.
5. Each change you make requires a commit—if you edit an existing document, you should commit at least once per sentence. If you create a new document, you can commit each paragraph. This allows you and others to accept or reject each individual change and enables you to explain why you made a certain change.

Example: `internal/guides/publish-on-medium`

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

If you're happy with all the changes in your new file, you can make a [pull request](../glossary/pull-request.md) and add the URL of your pull request—which you can find in the address bar of you browser—to the [achievable](../glossary/achievable.md) you just finished. Now your changes will be reviewed by somebody else who will either comment, add commits (changes) or [merge](../glossary/merge.md) the request (this means the file is good to go).

---

**1:**<img src="../images/pull-request.png" width="300">

---

**2:** <img src="../images/pull-request-button.png" width="200">

---

**3:**<img src="../images/right-branch.png" width="600">

---

**4:**<img src="../images/name-branch.png" width="400">

---

You created a create pull request! Congratulations! It feels great every time.

If somebody comments, the original owner and everybody who has commented/committed to the pull request will receive a notification (you can also choose not to receive messages in the GitHub settings).

### A shortcut when changing something small

When changing something small, you can go to the designated file and hit the *edit* icon. Do not commit directly on the ready branch, because that would be "illegal", but choose the option to *Create a new branch for this commit and start a pull request*.


### Discuss and merge

<img src="https://media.giphy.com/media/kFJ7NdGw4A4o0/giphy.gif" width="100%">

You can edit a pull request or comment on certain parts of the file by clicking the + sign on the left. When you click, your comment will be visible in the conversation menu.

When everyone is happy about the document and the file is fit to go to the ready branch, the person reviewing the pull request can push the big green *merge* button on the bottom of the conversation menu and press the *delete branch* button that appears after you have merged. Congratulations 🏅, The branch is *merged* with the `ready` branch and is fit to go live. High five 🙏!

## Working local on your own device

Working local means that you [clone](../glossary/clone.md) (i.e. copy) a repository from the GitHub client to your local device in your own designated folder.

You need to download [GitHub Desktop](https://desktop.GitHub.com/) and a text editor, for example: [Atom](https://atom.io/) (see our [Atom guide](../atom-guide/readme.md) for further consultation). A text editor comes in handy when writing a bunch of text or code.

[*Cloning a repository*](https://help.GitHub.com/desktop/guides/contributing/cloning-a-repository-from-GitHub-desktop/) means that you copy a repository from the browser on your device into your own folder architecture. You do this in your GitHub desktop application.

Make sure you select or create the right branch in the GitHub desktop.

***Never commit to the ready/live branch itself, unless you're fixing a breaking bug and you're 100% you don't break anything with the commit.***

Any change you make to a file in the folder (or subfolder) on your device results in an uncommitted change in GitHub Desktop. If you press *commit changes*, you in fact update your *local* branch. You now will have to *publish* your local branch in order share your changes with others. Press *Sync* to push the local changes to an existing online branch with the same name, or if you want to update your local branch with the content of the online branch.

So now there are two branches with the same name, one local and one online. Team members can't see your local changes and your local branch also doesn't automatically copy changes from the online branch. It takes an action from you to syncronise them.

Therefore, if you want to change or add a file, you *sync* with the most recent branch on that repo specific to what you are working on. This is often the `ready` branch if you create a new file, and always the same as your local branch if it already exists.

### Add images

You can only add images locally by saving them in the designated folder (e.g. images-folder).

---

<img src="../images/right-branch-desktop.png" width="300">

---

Then, you can open the relevant repository folder in your text editor. The following image shows text editor [Atom](../atom-guide/readme.me) with the local repository folder on the left panel and the preview window on the right.

---

<img src="../images/atom-example.png" width="600">

---

## The dreaded merge conflict

If two people changed the same lines in the same file, or if one person decided to delete it while the other person decided to modify it, Git simply cannot know which change is correct. Git will therefore mark the file as having a conflict, which you'll have to solve before you can merge. Git will tell you which line resulted in a merge conflict. You have to decide, along with the other person who merged the file, which version is correct or create a new combined version.

> [Atom](../atom-guide/readme.md) has a [package](https://atom.io/packages/merge-conflicts) that will display `<----READY` and `<----HEAD` around the lines that resulted in the conflict.

See [GitHub's how to](https://help.GitHub.com/articles/resolving-a-merge-conflict-from-the-command-line/) to deal with the merge conflict. You can also contact a team member in [Slack](../slack-guide/readme.md) if you're having trouble solving the merge conflict.

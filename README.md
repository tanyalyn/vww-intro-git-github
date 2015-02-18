# Intro to Git and GitHub
Presentation and supporting assets for the Vermont Works for Women SUIT Intro to Git and GitHub workshop.

See the repo we built in the slides here: [raearnold/hello-world](https://github.com/raearnold/hello-world)

We’re using GitHub’s desktop application for Git, so the difference between Git and GitHub may seem blurry. If it helps keep things straight in your head, the things we do in the desktop application are Git things—we could do them through the command line as well, and they are all about version control. Things we do through the browser will be unique to GitHub, and will focus more on collaborating with the world outside your project.

We won't cover the command line interface (CLI) in the workshop, but the slide deck contains the commands you need, in case you want to explore using the CLI in the future.

## What is Git?

Git is an open-source, **distributed** **version control system**.

A *version control system* allows you to keep track of changes to documents, making collaboration easy. *Distributed*, in this case, means that each user has a copy of the repository on their own computer that syncs with a remote server only when you're ready for it to do so. This makes changing files and storing them fast and provides numerous backups since every user has a copy on their own machine.

The distributed aspect (and its advantages) is one major difference between Git and the version control systems that came before it (such as CVS and Subversion), and one of the main reasons it has grown to be one of the most common version control systems in use today.

Version control systmes are widely used for things involving code, but you can version control images, documents, and any number of file types.

## What is GitHub?

At its most basic, GitHub is a web-based hosting service for Git **repositories** (think of a *repository* as a project, or collection of your files). But, GitHub is also part-social-network (for developers); part-all-in-one bug tracking tool; part-open-source-facilitator (everyone can see your code and can edit it if you allow it); and much more.

GitHub also allows you to host basic websites directly from your repositories. This is how we manage the Vermont Works for Women SUIT page.

## Git Basics

Commands we learn:

- Init
- Add
- Status
- Commit
- Reset
- Log
- Branch
- Checkout
- Merge

### Staging

The files in your repository on your computer are in what is known as your **working directory**. You can make whatever changes you want, but Git doesn't automatically track the changes—you have to tell it that you're ready to save a batch of changes. 
You do this by **staging** the changes you want using the **add** command. 

It's important to note that you can make a **commit** (a snapshot of changes that you tell Git to keep track of) out of any or all of the changed files in your working directory. When you commit, only the files you have staged will be included. The status command will show you the status of all your modified files, as well as the commands to stage or unstage them. In the GUI, it's as simple as checking or unchecking the files you want to commit.

### Branching 

Branches make it simple to work on experiments, major content changes, or bug fixes without danger of messing up existing work. You can continue to commit, but it won't change your main code base. Branches share all commits with their parent branch up to the point where they were created. Then, they diverge.

You use **checkout** to switch between branches, but you must commit any staged changes before doing so.

#### Branching Strategies

Different companies, developers, and repositories use different branching strategies. There's no one right way—it's largely dependent on the project.

In most cases (that is, all but the most simple projects), work shouldn't be done on the *master* branch. You should use branches (often referred to as **feature branches**) to work on features or bug fixes, then merge them into the master branch once they've been tested.

#### gh-pages

GitHub has a special branch name, *gh-pages* that allows you to create simple websites that are hosted on GitHub (like the slides for this presentation are). We don't have time to dig into setting all that up, but here is one good tutorial: [Getting to Know GitHub Pages on TutsPlus](http://webdesign.tutsplus.com/tutorials/getting-to-know-github-pages-static-project-pages-fast--webdesign-11501)

This is a great example of a branching strategy with a branch that might never be fully merged into *master* (or vice versa). In fact, some projects (that are stored on GitHub, at least) might only have a *gh-pages* branch—no *master* at all. Although this repo is not set up in that way, it could be.

### Merging

Branches aren't much help if they live off on their own forever. Merging allows you to integrate changes from one branch into another. Once you merge a branch in (and resolve any **merge conflicts** that occur), the original branch contains all of its own commits as well as any from the merged-in branch.

### Sidenotes

#### README.md files

It's a common practice to have a README.md file in all of your repositories. It can be very simple—just a quick description of the project or repository—or extremely detailed, containing coding standards, technical design standards, information about the community maintaining the repo and more. GitHub helpfully displays your README on the project's home page.

The **.md** format stands for [Markdown](http://daringfireball.net/projects/markdown/basics), which allows GitHub (and many other projects) to convert plain text to clean HTML. If you want to learn more about the syntax, that link explains everything. However, Markdown is pretty forgiving—you can just add plain text to your README—it won't be pretty, but you'll get the point across.

#### Commit Hashes

Each commit has a unique identifier known as a **hash**—it's that string of letters and numbers you see in your log. While we don't cover much about them in this presentation, you can use the full hash, or even just the first 6-7 characters of it, to check out specific snapshots, merge only portions of a branch into others, and much more.

## Collaboration

### Setting Up Remotes
So far, everything we've done has been on our own computer. There's not much collaboration.

This is where GitHub comes in. If we connect our local repository to a remote repo hosted by GitHub, suddenly we can share our code with others and work together.

Once you've set up your remote, you can view your project on GitHub, and even make simple edits in the browser.

Commands involved:

- Push
- Pull
- Remote

### Forking
GitHub only allows designated collaboraters to commit changes directly to a repository. 

If you want to commit to someone else's repo, or want to use one as a starting point for your own project, you have to **fork** it through GitHub.

Once you've forked it, you can clone it to your your computer and work on it using all the skills we've learned so far.

Commands involved:

- Clone

### Pull Requests
Once you've commited changes, you can use **pull requests** to ask the original project’s collaborators to incorporate your changes into their repository.

Things to keep in mind:

- Always read READMEs and any code standards documents in the project, and follow the guidelines they set
- Thoroughly test your changes before submitting a pull request
- If you're fixing a bug, make sure you connect the pull request to a bug reported on GitHub. If one doesn't exist, file it first, then fix it

## Lab Time

- Fix one typo in this presentation and submit a pull request
- Find something interesting, fork it, check out your fork locally

## Resources

[Git-scm.com](http://git-scm.com/) is the homepage of the Git project, that will direct you to many resources, GUIs, downloads, etc. 

[Try Git](https://try.github.io/levels/1/challenges/1) is a free introduction to Git that allows you to try the basic commands directly in your browser, thanks to Code School.

[Pro Git](http://git-scm.com/book/) by Scott Chacon and Ben Straub is available for free online. It's very comprehensive, and a go-to resource.


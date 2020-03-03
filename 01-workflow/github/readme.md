# Github

## Version control - what is it and why would we want to use it?

Perhaps you've had a class in school with a final project or essay. As you go through numerous drafts, and try out different strategies, you want to be free to try new things without the fear of losing your old writing just in case you need to go back or rework back in some stuff at a later time. Maybe your desktop looked like this:

**My-Essay.doc**

**My-Essay2.doc**

**My-Essay-New.doc**

**My-Essay-New2.doc**

**My-Essay-final.doc**

**My-Essay-final-version.doc**

**My-Essay-actual-final.doc**

**My-Essay-REAL-FINAL-VERSION.doc**

Don't tell us you can't relate! But wouldn't it be nice if we just had a program to handle any history or previous versions for us so we didn't have to keep a dozen copies of the same file? This is where version control systems come in. 

> The version control system we use is called `git` - it's the most popular version control system right now

## Who invented git?

Linus Torvalds - of Linux fame - invented git in 2005. You can read more about that [here](https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git) but the short version is that he invented it as a version control system for the community that was developing for the Linux operating system after the tool they used previously broke down.

> It may take awhile to truly believe this - but git was made to be simple and elegant (compared to other version control systems)!

## Git vs Github

Remember, *git* and *github* are two different things! Git is a version control system for managing your source code. Github is a platform to host your code online so others can access it and collaborate with you on it. You can think of Github as social media for Git! For a more detailed explanation, [watch this video](https://www.youtube.com/watch?v=uUuTYDg9XoI)!

## What git commands do I need to know about?

Let's cover a few basic things that Git and Github can do that are useful to know about. Let's try to cover these in the order that you might encounter them in a regular development process.

### Forking

What is a fork? When you visit a repository on Github, you'll see a button called "Fork" in the top right corner. It looks like this:

![](https://res.cloudinary.com/briezh/image/upload/v1583265934/Screen_Shot_2020-03-03_at_12.05.06_PM_ro1prf.png)

Forking is something you'll need to be logged in to Github to do. When you fork someone else's repository, a complete copy of that repository is made on your own account. This may feel a little weird at first, but in fact, openness, sharing, and cooperation is highly respected within the software development community.

> At GA we often have you make forks of starter code for homeworks!

### Clone

Once you have a "fork" of the repository on your own Github account, you want to clone the code onto your local machine so that you can open it up your text editor and work on it. During cloning all of the code in your Github repository (and all of the commits) will be copied onto your computer. You can initiate a clone by copying the clone link. This is a green button on the right of the page. Clicking the copy icon will automatically copy it to your clipboard, or you can highlight the text and press `Cmd + C`.

![](http://res.cloudinary.com/briezh/image/upload/v1531169741/Screen_Shot_2018-07-09_at_1.55.16_PM_kb0fuq.png)

Once you have this link copied, you can go to your terminal and type the following command in order to start the clone process: 

```bash
git clone THE_LINK_YOU_COPIED
``` 

> Tip: Don't clone into a location that is already being tracked by git

### Getting the Code Back to the Internet

So let's say you made some beautiful new code and now you're ready to let that code live it's best life out in the wilds of the internet. How do we get that code from our computer back up to Github?

Let's step back for a second. If you want to send your granny a birthday present, what kind of process do you need to go through?

1. We need a gift
1. We need to put the gift inside a box
1. We need to tape up the box
1. We need to give it to the mailman (or woman) with an address on it

We then trust the mail carrier to get the package to our granny with the address and instructions we've given. Let's use this metaphor of sending a physical package to describe the process of sending our code to Github.

### Add (Staging Changes)

In our metaphor, our new code changes are like the gift we're giving to granny. It's the thing we want to send. Continuing that metaphor the `git add` command is like placing that gift in the box. This is sometimes referred to as "staging changes". 

1. We need a gift **(Our new code)**
1. We need to put the gift inside a box **(Staging changes)**
1. We need to tape up the box
1. We need to give it to the mailman (or woman) with an address on it

You may see a couple variations of the add command:

`git add -A` (Add all changes from files in this repository)

`git add .` (Add all changes from the current folder all downward)

> Fun fact: from the root (top) folder of your project, these commands do exactly the same thing.

### Commit

TODO

### Push

TODO

### Pull Requests

## Relevant XKCD

![](http://res.cloudinary.com/briezh/image/upload/v1531164700/git_XKCD_y1vvzk.png)

## Activity Time!

Let's practice using Github together! Visit the [Pull Test Repo](https://github.com/WDI-SEA/pull_test) on GA Seattle's Github account. Your instructor will lead you through forking, cloning, pushing, and pull requests.

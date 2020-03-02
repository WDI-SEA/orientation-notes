# Terminal Tips and Tricks

## What is a terminal vs a console vs a command line interface?

These are all related concepts, and often for our purposes they're used interchangably! For our purposes, let's use the following definitions:

**Terminal**: The program on your Mac, Linux, or Windows machine that you will open.

**Console**: A general term for something that you might type commands into. Your terminal program is an example of a console, but your internet browser (Chrome or Firefox) or text editor (VS Code) also may have a console that you can type commands into as well.

**Command Line Interface**: Any program that you might use that has specific commands you can type into a console. We've already seen in the prework that we can type commands that start with the word `git` in order to do different things with git. For example, `git push origin master` is one that we've used in order to "push" code from our local computers to our Github repositories.

**Shell**: The shell is the command line interpretter. Essentially it's how your computer makes sense of whatever is being typed in your terminal. You can think of it as a program whose primary purpose is to run other programs. Some common shell flavors are `bash` (Bourne Again SHell) and `zsh` (Z-SHell). Bash is pretty pervasive, but for MacOS the Catalina update resulted in a shift from bash to [zsh as the terminal default](https://scriptingosx.com/2019/06/moving-to-zsh/). Zsh has some nice features bash doesn't, and we've always used zsh at GA Seattle anyway, so this is a convenient change!



> If you'd like to dig further into the differences, take at look at this forum post on [AskUbuntu.com](https://askubuntu.com/questions/506510/what-is-the-difference-between-terminal-console-shell-and-command-line)!

## How do I even open this thing? I'm scared.

On a Mac, you may be accustomed to opening up your `Applications` folder and hunting around for the program that you need. There are a couple even quicker ways you can open programs (including your terminal program). 

#### 1. Swipe all fingers from the outside of your trackpad to the inside

It's a little hard to describe, but it looks like a grasping motion. Imagine that there is a marble in the middle of your trackpad that you're trying to grab. This will bring up a screen with all of your applications. Simply click on the one that you want.

#### 2. The `⌘` + `SPACEBAR` keyboard shortcut

This brings up a textbox that you can start typing the name of the program you're looking for. This is called "Spotlight Search" and it looks something like this:

![](https://res.cloudinary.com/briezh/image/upload/v1583171079/Screen_Shot_2020-03-02_at_9.42.56_AM_tzo84y.png)

Once you've started typing, you'll see anything that matches what you've typed. In my case, I'm looking for "Terminal" so I've typed "Ter" which has incidentally also matched anything about "Teriyaki" I've ever looked for:

![](https://res.cloudinary.com/briezh/image/upload/v1583171079/Screen_Shot_2020-03-02_at_9.43.08_AM_yq9l0u.png)

**Activity: Let's try this out together now**

* Press and hold the command key followed by the spacebar
* Start typing the word `terminal`. You probably only need two or three letters for it to narrow it down to the program you want.
* Once the terminal program pops up, select it

There we go! You're in the terminal now! Keep it open, we'll be learning some commands you can type into the terminal next!

## Some Common Commands

The first and most important things to learn about the terminal is how to see where you are and navigate around.

**Where am I?**

`pwd` is short for "Print Working Directory". It will show you the path from your root to where you are currently.

> Quick aside: "Directory" and "folder" will be used interchangably in this course! Many of the abbreviations for commands use `d` for directory. 

![](https://res.cloudinary.com/briezh/image/upload/v1583173059/Screen_Shot_2020-03-02_at_10.17.17_AM_bmwfmn.png)

You'll notice that the absolute path to where I am in my file system starts with a `/`. This is used to denote the "root" level of my local computer. 

**List directory contents**

`ls` is the command to list your directory contents. Go ahead and try it out now. 

The `ls` command, like many commands accepts arguments called "flags". These optional arguments will start with a dash and may be combined with other flags. For example, the `-l` flag (`ls -l`) will list details about each file and folder. Notice the difference between `ls` and `ls -l`:

![](https://res.cloudinary.com/briezh/image/upload/v1583174406/Screen_Shot_2020-03-02_at_10.39.19_AM_dk96gb.png)

The `-a` flag will allow you to list normally hidden files that start with a `.` 

We can combine the two flags into a command `ls -la` as well. 

> Feel free to explore the [many other flags and options you can use with the ls command](https://www.techonthenet.com/unix/basic/ls.php), but just these two flags will get you by in the class just fine! 

**Change directory**

TODO: CD

A moment ago we referenced `/` to refer to your computer's root directory. On the other hand, the `~` symbol is used to denote the "home" directory, which is sort of like a user-specific root. For me, my home directory is `/Users/brandiwilliams`. Check it out.

![](https://res.cloudinary.com/briezh/image/upload/v1583173760/Screen_Shot_2020-03-02_at_10.27.23_AM_kk3aag.png)


## Some Tips

**Tab Completion*

Do you enjoy typing? Yeah neither do we. You can do a whole lot less of it on the terminal if you use tab completion. If you're typing a file name and let's say it's a really long name then you can type the first couple letters and press `TAB`. If there are no other matching filenames, voila, it's automatically filled in for you! If there is more than one match, you'll see them all and be able to tab through them!

TODO: IMAGE OF TAB COMPLETE

**History**

So your computer remembers the commands you've used previously... we can use this to our advantage because as you'll notice throughout the course, you'll be using the same commands a lot! By using the up and down arrows, you can go back through your previous commands. 

TODO: IMAGE OR GIF

TODO: TRY IT OUT YOURSELF

Additionally, this becomes more useful because you can essentially filter your past commands by typing a part of it. For example, say you'd like to look at old `git` commands you've used. If you type the word `git` first and then proceed to use the up arrow you will be going through only your past commands that started with the word `git`. Neat huh?

## Setting Up Your File Structure for Success

TODO: EXPLAIN IMPORTANCE OF ORGANIZATION

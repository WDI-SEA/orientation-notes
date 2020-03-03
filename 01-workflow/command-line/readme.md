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

## Useful Common Commands

### Navigation

The first and most important things to learn about the terminal is how to see where you are and navigate around.

**Where am I?**

`pwd` is short for "Print Working Directory". It will show you the path from your root to where you are currently.

> Quick aside: "Directory" and "folder" will be used interchangably in this course! Many of the abbreviations for commands use `d` for directory. 

![](https://res.cloudinary.com/briezh/image/upload/v1583173059/Screen_Shot_2020-03-02_at_10.17.17_AM_bmwfmn.png)

You'll notice that the absolute path to where I am in my file system starts with a `/`. This is used to denote the "root" level of my local computer. 

**What's in here?**

`ls` is the command to list your directory contents. Go ahead and try it out now. 

The `ls` command, like many commands accepts arguments called "flags". These optional arguments will start with a dash and may be combined with other flags. For example, the `-l` flag (`ls -l`) will list details about each file and folder. Notice the difference between `ls` and `ls -l`:

![](https://res.cloudinary.com/briezh/image/upload/v1583174406/Screen_Shot_2020-03-02_at_10.39.19_AM_dk96gb.png)

The `-a` flag will allow you to list normally hidden files that start with a `.` 

We can combine the two flags into a command `ls -la` as well. 

> Feel free to explore the [many other flags and options you can use with the ls command](https://www.techonthenet.com/unix/basic/ls.php), but just these two flags will get you by in the class just fine! 

**Get me out of here**

The `cd` command stands for "change directory". It's followed by the location you wish to change to, which must be the name of a directory. For example, in the above example while we were discussing the `ls` command, I was in a folder called `doughnut-shoppe` and I saw inside it a folder called `controllers`. If I wanted to change directory location to that controllers foldeer, I would use the command `cd controllers`. I can also specify a path. For example I could specify `cd controllers/subfolder` if I want to get to a folder called "subfolder" inside of the "controllers" folder.

If I wish to back out of a folder, I can use the special designation of `..` (two dots) to reference a parent folder. If I am in the "controllers" folder and I wish to go back up to the "doughnut-shoppe" folder, I can use the command `cd ..`. I can also use this in a path, so for example, if I am currently in the "controllers" folder but I want to get to the "models" folder (which is a sibling folder also located inside the "doughnut-shoppe" folder), I can use the command `cd ../models`.

A moment ago we referenced `/` to refer to your computer's root directory. On the other hand, the `~` symbol is used to denote the "home" directory, which is sort of like a user-specific root. For me, my home directory is `/Users/brandiwilliams`. Check it out.

![](https://res.cloudinary.com/briezh/image/upload/v1583173760/Screen_Shot_2020-03-02_at_10.27.23_AM_kk3aag.png)

**Clear the screen**

If you have too much information and clutter on your screen, you can use the `clear` command to get a fresh empty screen.

### Creating/Removing Files and Folders

**Making a new directory**

Let's create a new folder together using the `mkdir` command (short for "Make directory"). We'll go ahead and set up a file structure we can use for the course.

1. Change directories to your home directory using the command `cd ~`
1. Make a new directory called `code` (or `GA` or `SEI` if you prefer)
1. Change directories to your new `code` directory using the command `cd code`
1. Make 4 new folders with the following commands - one this orientation class and one for each unit in SEI
  * `mkdir orientation`
  * `mkdir unit1`
  * `mkdir unit2`
  * `mkdir unit3`
  * `mkdir unit4`
1. Change directories into your `orientation` directory that you just created using the command `cd orientation`
1. Create 2 new directories - one for labs and assignments and one for code-alongs
  * `mkdir labs-and-assignments`
  * `mkdir code-alongs`
  
This should be a pretty nice structure for us to use for the remainder of the class. 

**Making a new file**

You can make a new file using the `touch` command followed by the name of the new file you wish to create. Following the previous activity, we should now be in a folder called `orientation`. Let's continue the activity using the new touch command.

1. Type `pwd` to see where you're at. Make sure that the path starts with your home folder (for me, that's `/Users/brandiwilliams` - for you, it will likely be `/Users/<YOUR NAME>`)
  * My full path is `/Users/brandiwilliams/code/orientation`
1. Change directories into the `code-alongs` folder by using the command `cd code-alongs`
1. Create a new file called `test.txt` with the command `touch test.txt`
1. Use the `ls` command - do you see your new file?
1. Create a new file called `myfile.txt` with the command `touch myfile.txt`
1. Create a new file called `history.txt` with the command `touch history.txt`
1. Use the `ls` command - do you see all three files?

**Removing a file**

Perhaps we didn't actually mean to create that test.txt file. Oops! Luckily we can delete it with the `rm` command. Try running the following command: `rm test.txt`. Run `ls` again and it should now be gone!

**Removing a folder**

You may want to refrain from using this one. Doing a delete on the command line can't be undone, and it won't stop and ask you if you're sure like deleting a folder via your GUI normally would. The command for deleting a folder is also `rm` but it must be specified with the `-r` command to indicate recursive deletion. This is because deleting a folder deletes all files *and folders* inside it, and of course all files *and folders* inside of the subfolder... and so on!

> GUI means "Graphical User Interface" - you know, like your mouse and pointing and clicking, etc

Again, we'd highly recommend waiting until you're more comfortable with working in the terminal before using this one!

### Writing and Routing

**Echo! (echo!)**

Try typing this command: `echo "hello world"`. It seems rather silly doesn't it? It just repeats back what you've written. What's the point of that? Hold that thought!

**Writing and Appending to Files**

There are two operators that allow us to write to a file: `>` (over)write and `>>` append. try out these commands and then quiz yourself below:

* `echo "Hello world line 1" > myfile.txt` (write)
* `echo "Hello world line 2" >> myfile.txt` (append)
* `echo "Hello world line 3" > myfile.txt` (write)
* `echo "Hello new file" > newfile.txt` (write)

**mini-quiz**

<details>
 <summary>What do you expect the contents of `myfile.txt` to be?</summary>
 <br />
 It turns out that we are completely overwriting the contents of myfile.txt with the command `echo "Hello world line 3" > myfile.txt`, so all we'd expect to be in there at the moment is "Hello world line 3".
 <br />
</details>

<details>
 <summary>Do you think `newfile.txt` was created or does a file have to exist in order for us to write to it?</summary>
 <br /> 
 In this case, luckily the file is auto-created if it doesn't exist already. Convenient! 
 <br />
</details>


**Here kitty kitty**

No, not that type of cat! `cat` is a command that allows you to read the contents of a file! Let's take a look at the file "myfile.txt" using the command `cat myfile.txt`. We should see the content we just wrote to it with our echo, write, and append commands in the previous step.

It also turns out, we can put multiple files together for viewing purposes with cat. Try this out: `cat myfile.txt newfile.txt` - you should see the contents of both files!

![](https://res.cloudinary.com/briezh/image/upload/v1583193727/Screen_Shot_2020-03-02_at_4.01.38_PM_p0ecxq.png)

**The history command**

`history` is a command that will tell you the previous commands that you've typed before. Try it!

![](https://res.cloudinary.com/briezh/image/upload/v1583194264/Screen_Shot_2020-03-02_at_4.10.36_PM_kskfaz.png)

**The pipe operator**

Did you notice the `|` operator in the screenshot above? This is called a "pipe". Think of a pipe as taking data from one place to another... just like pipes in Mario games take Mario from one place to another. Whee!

![](https://res.cloudinary.com/briezh/image/upload/v1583194914/mario_raut7v.jpg)

So, essentially in the command `history | tail`, we're taking the data from the `history` command, which is a long list of commands that I've run in the past, and feeding it into the `tail` command. `tail` takes the last 10 lines fed into it and spits it back out. Thus, I can view only the last 10 lines instead of the whole thing.

> Note: `head` does the opposite of `tail` - it takes from the beginning!

**Anding**

You can string together commands using the `&&` operator. Try this out: `cd .. && ls -l`

## Some Tips

**Tab Completion*

Do you enjoy typing? Yeah neither do we. You can do a whole lot less of it on the terminal if you use tab completion. If you're typing a file name and let's say it's a really long name then you can type the first couple letters and press `TAB`. If there are no other matching filenames, voila, it's automatically filled in for you! If there is more than one match, you'll see them all and be able to tab through them!

TODO: IMAGE OF TAB COMPLETE

**History - using the up and down arrows**

So we saw above that your computer remembers the commands you've used previously... we can use this to our advantage because as you'll notice throughout the course, you'll be using the same commands a lot! By using the up and down arrows, you can go back through your previous commands one at a time! 

Additionally, this becomes more useful because you can essentially filter your past commands by typing a part of it. For example, say you'd like to look at old `git` commands you've used. If you type the word `git` first and then proceed to use the up arrow you will be going through only your past commands that started with the word `git`. Neat huh?

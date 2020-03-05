# Machine Setup

## Some Installations

Let's do a few installations from the command line. 

### Homebrew (Mac only)

First, for Mac users, we're going to be using an installer called "Homebrew". This will allow us to use the "brew" command for any future installations.

> If you're on Linux, you'll be using the "apt-get" command instead of "brew". You don't have to do anything to set it up. Lucky you! While you wait feel free to either skip down to installing Node or gloat smugly, whatever your jam is.

Mac users, open up your terminal and run the following command: (please copy and paste it!)

```sh
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

> Note: You may be prompted to install xcode. Agree to this, but know that it might take a couple minutes, especially on older Macs.

### Xcode (Mac only)

You may have already been prompted to install this when installing homebrew. If not, go ahead and run it now:

```sh
xcode-select --install
```

> Note: This one may take a few moments. It's an ideal time to go grab a refill of water or coffee.

### Node

TODO

### Python

TODO

### PostgreSQL

TODO

### MongoDB

**Notes:** The name of the free version of MongoDB has changed to `mongodb-community` as of November 2019. Also, the Catalina version of MacOS (version 10.15) disallows folders being created at the root of the file system so you must create your MongoDB data folder inside your home folder.

```sh
#Install MongoDB
brew install mongodb-community

#make data directory
sudo mkdir -p ~/mongodb-data
```

After creating the data directory in your home folder, it should be marked with your correct ownership permissions but if you find that it is owned by root instead, you can change it to be owned by you with the following commands:

```sh
# Get your user name
whoami

# set data directory permissions (replacing USERNAME with the result from whoami above)
sudo chown -R USERNAME:wheel ~/mongodb-data
```

Finally, to tell MongoDB to start using the data directory that you just created, you must start it with the following command:

```sh
mongod --dbpath ~/mongodb-data
```

To make a shortcut for this command, open your ~/.zshrc (or ~/.bashrc if not using ZSH) and add this line to the bottom:

```sh
alias mongod="mongod --dbpath ~/mongodb-data"
```

#### Testing your MongoDB server

```sh
# Start the MongoDB server
mongod
```

Press `CTRL + C` to stop the server.

## Command Line Shortcuts

Now that we know a little bit about using the terminal, let's create some shortcuts in order to make our lives easier. Many times you will want to open up your current location in your text editor of choice. Let's make shortcuts for VS Code and/or Sublime Text and/or Atom.

**Sublime Text***

```bash
ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/local/bin/subl
```

**Atom**

```bash
ln -s /Applications/Atom.app/Contents/Resources/app/atom.sh /usr/local/bin/atom
```

**VS Code**

1. Open up your terminal
1. Open up your Z-Shell config file with the following command: 
  * `open ~/.zshrc`
1. Add the following line to the file:
  * `export PATH=$PATH:"/Applications/Visual Studio Code.app/Contents/Resources/app/bin"`
1. Save and close the file

**Last step**

In order to have these shortcuts take effect, we need to fully restart the terminal. Go ahead and go up to the bar at the top and click Terminal -> Quit Terminal. You can now reopen it with the spotlight search as we did earlier. The commands will now work as follows:

 * `code .` opens the current folder in VS Code
 * `subl .` opens the current folder in Sublime Text
 * `atom .` opens the current folder in Atom
 

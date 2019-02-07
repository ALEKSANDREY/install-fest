# Installfest

This guide will walk you through installation for all required software packages. So make sure you read the instructions first before you get started!

Despite what you've heard there are only a few differences in the commands you'll use to get setup. Otherwise you and your peers should share relatively similar experiences. 

For Ruby and Node, it's highly recommended to install Ruby Version Manager (RVM) and Node Version Manager (NVM). You can use these tools to install any version of Ruby or Node in a much simpler way. However, please ask your instructor what they recommend. To install them:

- RVM ([Docs](https://rvm.io/rvm/install))
- NVM ([Docs](https://github.com/creationix/nvm#installation))

If you use these, follow only the instructions below for RVM/NVM to install Ruby and Node.

Required software we'll be installing in this guide:

* Ruby ([Docs](https://www.ruby-lang.org/en/documentation/installation/#apt))
* Node ([Docs](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions))
* Rails ([Docs](https://github.com/rails/rails#getting-started)) - Install  instructions only! 
* Postgres ([Docs](https://www.postgresql.org/download/linux/ubuntu/))
* MongoDB ([Docs](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/))
* Git ([Docs](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git))

You should always refer to the official documentation if you encounter problems with installing the software. This guide will walk you through installation of each package.

Additional dev tools:

* OhmyZSH ([Docs](https://github.com/robbyrussell/oh-my-zsh#getting-started))
* Sublime ([Docs](https://www.sublimetext.com/3))  or Atom ([Docs](https://atom.io/))
* Google Chrome
* Tree
* Nodemon

Additional resources:

- [PostgreSQL](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04)


## Getting Started

First things first: before you install new software, always update your system.

```
# Always use this command before installing new packages.
# It updates a list on your system of available packages. It does not install anything.
sudo apt-get update

# Use this regularly (daily/weekly/monthly) to keep your system up-to-date
# It uses the list of available packages to install updates.
sudo apt-get upgrade -y

# A handy tool that provides a tree-like, readable view of folder contents
sudo apt-get install tree
```

These commands will download and install updates to your packages in addition to applying system wide upgrades.


### Installing Sublime or Atom (recommended)

If you've already got a code editor that you love and are comfortable with, you're more than welcome to continue using it! Sublime and Atom are free alternatives and your instructors are able to provide you with more advice and support if you use them.

You can install Sublime Text from the *Ubuntu Software Center* (search for it in the menu). 

For Atom:

```
curl -L https://packagecloud.io/AtomEditor/atom/gpgkey | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] https://packagecloud.io/AtomEditor/atom/any/ any main" > /etc/apt/sources.list.d/atom.list'
sudo apt-get update
```

### Installing and Configuring Git

```bash
sudo apt-get install git-all

# Now we will configure it:
git config --global user.name "YOUR_GITHUB_USERNAME"
git config --global user.email "YOUR_GITHUB_EMAIL_ADDRESS"
git config --global credential.helper cache

# IMPORTANT: Use the name of your preferred text editor!
# For atom use: "atom"
# For sublime use: "subl"
git config --global core.editor "your_editor_here"
```


### Installing OhmyZSH (recommended)

ZSH is optional, but highly recommended. In short, it makes using the command line easier for you by providing more information and a lot of shortcuts. It also improves how things look by adding color coded messages and formatting to your inputs and outputs.

```bash
sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"
```

That should be it. Once installed, close your current terminal window and open a fresh one. You should see a small difference in how your command prompt looks and you may even see a message to update ZSH.


### Installing RVM and NVM

```bash
# NVM: This will manage your node versions. Copy and paste the commands below:
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash
nvm install 8.9.4

# RVM: Will manage your Ruby and Rails versions. Copy and paste commands below:
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable --ruby

rvm install 2.5.0
gem install rails
```

That should do it.


### Install Everything Else

Copy and paste each command below, 1 by one. If you get an error message stating that the installation failed, check the documentation linked above. If that doesn't help, contact your instructor.


```bash

# PostgreSQL Database
sudo apt-get install postgresql postgresql-contrib libpq-dev
sudo apt-get install npm
npm install -g npm
npm install -g nodemon

# MongoDB: Copy and paste the commands below:
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 2930ADAE8CAF5059EE73BB4B58712A2291FA4AD5
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.6 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.6.list
sudo apt-get install -y mongodb-org

# SKIP THE COMMANDS BELOW IF YOU INSTALLED RVM and NVM.
# Ruby
sudo apt-get install ruby-full
ruby --version  # verify installation
sudo gem install rails

# Node
curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash -
sudo apt-get install -y nodejs
node --version  # verify installation

```


## Additional Tools

### Editorconfig (optional)

This will not impact your ability to keep up with the course work. It's just a very handy tool to help you keep your code in check.

This is a very handy little tool that you use with your code editor. It makes sure that your code is automatically formatted to the proper spacing and indentations.

Its just a text document that you add to your project folders. You add any settings you like and your code editor will use it whenever you're coding on the project.

Read about it: http://editorconfig.org/

Try it out!


### Sublime Packages (recommended)

These will not impact your ability to keep up with the course work. It's just a very handy tool to help you keep your code in check.

These packages will enhance your Sublime Text experience by providing some really handy tools. These are optional, but highly recommended.

First install the Package Manager: https://packagecontrol.io/installation

Then you'll be able to use it to install the following:

- Editorconfig
- Emmet
- SublimeLinter - jsl, ruby, jsxhint
- Gitgutter
- BracketHighlighter
- FoldFunctions
- Terminal (CTRL/CMD + SHIFT + T)
- Ruby Completions
- Javascript Completions
- jQuery (auto-complete feature)
- A nice theme (totally optional and fun!)

Keyboard shorcuts: http://docs.sublimetext.info/en/latest/reference/keyboard_shortcuts_win.html


### Atom Packages (recommended)

These will not impact your ability to keep up with the course work. It's just a very handy tool to help you keep your code in check.

- Emmet
- atom-beautify
- Linter (linter-rubocop, linter-eslint)
- Autocomplete (autocomplete-css, autocomplete-ruby)
- Highlight Selected
- Pigments
- Atom Terminal
- A nice theme (totally optional and fun!)

Keyboard shortcuts: https://flight-manual.atom.io/using-atom/sections/moving-in-atom/

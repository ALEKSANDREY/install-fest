# Installfest for Windows: Welcome to the Party

## You've Got Choices

The majority of the tools we use in this course *exist* for Windows, but many of them work slightly differently.

#### There are some options for how you might proceed, listed in order of best-likely-outcome to worst-likely-outcome.

### 1. Install Linux

Because Linux and MacOS are both Unix-based systems, the tools we use in this course are also available and will work in the same ways as Macs for Linux. While your instructor still won't be able to troubleshoot installation issues, or tell you what steps to follow to install pieces of software, you will be able to run the tools used in this class.

If you're comfortable setting up your computer to dual-boot Linux, that has been most effective for GA students in the past. Or, if partitions make you cranky, some students have been successful using VirtualBox to install a Linux VM; this is likely to cause you more issues than dual-booting, but it requires less know-how.

To install Ubuntu Linux: https://www.ubuntu.com/download/desktop
Continue to the setup instructions for Linux if you'd like to take this route.

### 2. Use Windows and Git Bash

Git Bash is a tool provided by GitHub to mimic the functionality of a Unix-based system on a Windows machine. This choice will require you to investigate for yourself how to install and run each of the tools we use in the course; you'll be installing the Windows version of those tools, then attempting to use them from a combination of the Windows shell and the Git Bash shell. I have seen one student attempt this setup before, and by the middle of the course, they bought a Mac, because they had run into so many issues with the slight differences between how frameworks and applications run on the different operating systems.

To install Git (with Git Bash): https://git-scm.com/downloads

Open your terminal and follow the instructions here to configure git. Use your regular, non-general assembly github account:
```
$ git config --global user.name "YOUR_GITHUB_USERNAME"
$ git config --global user.email "YOUR_GITHUB_EMAIL_ADDRESS"
$ git config --global credential.helper cache
```

Now let's install the following for your version of Windows:

- Ruby: https://rubyinstaller.org/
- Postgres DB: https://www.enterprisedb.com/downloads/postgres-postgresql-downloads#windows
- Nodejs: https://nodejs.org/en/download/
- Mongodb: https://www.mongodb.com/download-center#community

The above are the main tools that you'll need installed in order to use the additional tools below! So make sure you finish those up before moving on.

Next, open your Git Bash terminal and type the following commands, one by one:
```
gem install rails
npm install -g nodemon
```

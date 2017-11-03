# Church Connect Mobile App [![Build Status](https://travis-ci.org/churchconnect/mobile-app.svg?branch=master)](https://travis-ci.org/churchconnect/mobile-app)

This is a javascript application built on the aurelia framework. We use cordova / phonegap to build the javascript into a native iOS / Android application.

For instructions on how to build and deploy this application for a new church, see the `DEPLOYMENT.md` file.

## Development Requirements:

To develop this application, you will need:

* Node/NPM (node version 5.7.1 recommended). We recommend you install it using [nvm](https://github.com/creationix/nvm)
* Aurelia CLI: `npm install -g aurelia-cli`

## Setup

<<<<<<< HEAD
<<<<<<< HEAD
# Notes

* If you encounter conflicts during any merges or rebases or anything else, just make up the resolution as best you can. Since you don't understand the code, it will be hard to accurately resolve the conflicts. But you're being graded on your git work, not the coding, so just make sure the git actions work out.
* If you clobber any of the following files on your master branch, download them again and commit them back up to reset. (I won't grade you on how many times you add these back. As long as the test script works (and you haven't modified it), I'll be grading based on how many of the tasks you are able to complete).
    * The `README.md` file
    * The `.travis.yml` file
    * The `git-assignment-tests.sh` file
    * Also note that you hopefully won't clobber these files as each task is given its own branch.
* The following git alias will make inspecting the logs much easier:
    * Configure the alias with the following command: `git config --global alias.lp 'log --oneline --graph --all'`
    * Use `git lp` to get a more useful and powerful log output. :)
=======

# Notes

If you encounter conflicts during any merges or rebases or anything else, just make up the resolution as best you can. Since you don't understand the code, it will be hard to accurately resolve the conflicts. But you're being graded on your git work, not the coding, so just make sure the git actions work out.

The only exception to making up resolutions are:

### TODO: include links to these files.

* The `README.md` file
* The `.travis.yml` file
* The `git-assignment-tests.sh` file

For these files, just make sure they are look the same as the ones on my repository. They will need to stay the same. If you end up clobbering one of them, just wget them from the links above and commit them back up again on your master branch and you should be good. (I won't grade you on how many times you add these back. As long as the test script works (and you haven't modified it), I'll be grading based on how many of the tasks you are able to complete.
>>>>>>> parent of 5b7a450... Update task 1 now that we are using branches.

# Tasks
## TODO: task 1 may need to come last, since it kinda relies on master being the only branch from the password commit.

## Task 1:
* grep the git log for the commit that adds a "root password"
* Remove that commit using either the rebase or the cherry pick approach from this website: https://www.clock.co.uk/insight/deleting-a-git-commit
    * the rebase approach command example reads as such: `git rebase --onto <branch name>~<first commit number to remove> <branch name>~<first commit to be kept> <branch name>`
    * another way to say it is `git rebase --onto <new source commit> <old source commit> <branch you are rebasing>`
    * another way is: `git rebase --onto <commit hash before the password commit> <commit hash after the password commit> <branch you are removing the password from>`
* Note: pay close attention to the output of the rebase command and the output of git status when it hits a stopping point. Most of the time git tells you what you need to do next.
* Here's a more in-depth explanation of the rebase command for your enlightenment: https://git-scm.com/book/en/v2/Git-Branching-Rebasing



# Task 2:
* Simple rebase...

# Task 3:

* checkout the commit with this message: "object caching on the client side!" and create the branch `task-3` from that commit.
* push up the new `task-3` branch. This will require setting the upstream branch, but git will help you with the command to do that.


# Git Resources:

* How to remove a commit: https://www.clock.co.uk/insight/deleting-a-git-commit
* In depth on rebasing: https://git-scm.com/book/en/v2/Git-Branching-Rebasing
=======
The full development stack requires the API, the app (this repo), and,  our UI components library. However, for most simple tasks, you may only need to modify the app. The app is flexible enough to allow you to only work on the pieces that you actually need to change at any given point in time.

### The app (this repo)

* install node dependencies: `npm install`
* run the application locally (also watches files for changes): `npm run watch`

### API (optional)

You can develop against any running API by changing the `apiUrl` value in the `src/common-config.js` file. If you need to develop against a local API, review the installation instructions in the [API repository](https://bitbucket.org/sharptop/church-connect-api) and point the apiUrl at the local API instance.

### UI Components (optional)

* Aurelia UI Components contains a set of reusable components for this app. If adding a reusable component, add it to the UI components.
* While the library is new, modifications to it will be frequent. As it matures, the need to locally develop on the UI components will diminish.
* This is optional because the default setup of the app installs the UI components from bitbucket. The following instructions will change that.
* Clone the [ui components library](https://bitbucket.org/sharptop/aurelia-ui-components). 
* `npm install` to install its dependencies.
* `npm link` to make the global install of this package use your working directory.
* `npm run build` to build the library.
* go back to the church-connect-app directory, and `npm link aurelia-ui-components` to tell the app to use your local version of the ui components.
* When you make a change to the UI components, `npm run build`, then kill the `npm run watch` in the app, and restart it.

>>>>>>> parent of 925eed4... Add the assignment and test script and corrected travis configuration

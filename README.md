# Church Connect Mobile App [![Build Status](https://travis-ci.org/churchconnect/mobile-app.svg?branch=master)](https://travis-ci.org/churchconnect/mobile-app)

This is a javascript application built on the aurelia framework. We use cordova / phonegap to build the javascript into a native iOS / Android application.

For instructions on how to build and deploy this application for a new church, see the `DEPLOYMENT.md` file.

## Development Requirements:

To develop this application, you will need:

* Node/NPM (node version 5.7.1 recommended). We recommend you install it using [nvm](https://github.com/creationix/nvm)
* Aurelia CLI: `npm install -g aurelia-cli`

## Setup

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

# Tasks

## Task 1:

* There is a password commited at the beginning of the `task-1` branch. That commit needs to be completely removed.
* Remove that commit using either the rebase or the cherry pick approach from this website: https://www.clock.co.uk/insight/deleting-a-git-commit
    * the rebase approach command example reads as such: `git rebase --onto <branch name>~<first commit number to remove> <branch name>~<first commit to be kept> <branch name>`
    * another way to say it is `git rebase --onto <new source commit> <old source commit> <branch you are rebasing>`
    * another way is: `git rebase --onto <commit hash before the password commit> <commit hash after the password commit> <branch you are removing the password from>`
* Once you are done removing the commit, use the force to push your changes (git push -f origin task-1)
* Notes and hints:
    * When you do git log, you hit `/` to search for words. So `/password` should find you the commit containing the password. 
    * You can also use `git log | grep 'password'` to find the commit hash.
    * Note: pay close attention to the output of the rebase command and the output of git status when it hits a stopping point. Most of the time git tells you what you need to do next.


# Task 2:

* the last two commits on the `task-2` branch need to be removed.
* use the `git reset` command to remove the two commits (google should help you figure out the precise options to use to remove the two commits).
* Once you are done, use the force to push your changes.

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

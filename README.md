# NodeJSExample
Simple example and tutorial on how to set up a Node.js website with Express.
This project is a simple node.js example
sources:
https://www.youtube.com/watch?v=ENrzD9HAZK4
https://www.youtube.com/watch?v=HkdAHXoRtos

To check node version: 'node -version'
To run a file: 'node filename.js' or to run index.js just 'node .'

Nodes in-built file system is called fs.

To export functions from another module use: 
In index.js:
const myModule = require('./myModule'); //if in the same directory, if not write the path
In the module file write:
module.exports = {
    myFunction
};
This lets you use myFunction in index.js

NPM:
Lets you use packages
To initialise it in your project, write in the terminal: 'npm init -y'
This will create a package json file

A very popular and useful package is 'express'
To install write in the terminal: 'npm install express'
Adding this package will add a 'package-lock.json' file and a node_modules folder.

To import express write in index.js:
const express = require('express');
const app = express();

To tell express you want to use the files in the folder 'public' write in index.js:
app.use(express.static(_dirname + '/public'));

Git and GitHub:
Assuming you're using visual studio code:
Once downloaded git, click the source control button on the side of visual studio code or

'git init' to intialise the project, this will add all existing files to the changes panel
'rm -rf .git' uninitialises git if you want to remove the repository

Downloading GitLens is helpful for vscode too

Gitignore:
Creating a '.gitignore' is helpful as it removes certain files from your source control
Add '/node_modules' to this file to remove the 'node_modules' folder
To help make a .gitignore file, install the gitignore extension by CodeZombie
Then search '>git' and click 'Add gitignore' and type 'Node' to get the node.js gitignore template

Commits:
To make a commit type in the terminal: 'git add .' to prepare to commit all files (stage)
'git reset .' will reverse (unstage) these files
A tip is to make small commits
To commit: 'git commit -m "message goes here"' (the -m adds the message flag)
Or click the commit button in vscode

Branches:
'git branch' tells you all the current branches
You can create branches to experiment or fix bugs then merge it to the master branch when you're ready
To create a new branch you use 'git checkout -b branch-name'

'git stash -u' saves changes but doesn't commit them
'git stash pop/apply' will either pop or apply these changes

'git merge branch-name' merges the branch to master
'git merge branch-name --squash' commits all the changes as one when merging
This won't always work though, which leads to merge conflicts

GitHub:
You can push changes to GitHub, which I like to do through the app

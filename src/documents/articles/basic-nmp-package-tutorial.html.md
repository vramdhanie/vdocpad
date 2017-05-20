```
title: Create Your Own NPM Package
layout: article
tags: ['npm','build', 'package', 'tutorial', 'deploy', 'javascript', 'article']
description: Quick step by step instructions for creating and deploying a simple npm package.
icon: fa-database
```

## Introduction
This is a tutorial about creating, deploying and managing your own npm packages. 
We will develop a simple package that takes a string and shortens the string to less
than some predefined number of characters and add ellipses to the end. So if you
have a long string you can shorten it for display.

### Setup
The first step is to setup your working directory, setup npm and git. 

#### Directory
Create a directory named _shorten_.

``` bash
mkdir shorten
cd shorten
```

#### Initialize npm
Run the initializer for npm providing appropriate values for the project.

``` bash
npm init
```

This script will prompt for a number of values which should be obvious. 
The defaults are usually good enough so if you are not sure just accept the defaults. 
You will be able to change these values later
if you wish so no worries if you change your mind.

Npm will create a file named _package.json_ with the details at the end of the process. Here is
the content of my file:

``` javascript
{
  "name": "shorten",
  "version": "0.0.1",
  "description": "Shorten strings to manageable lengths",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [
    "string",
    "shorten",
    "ellipses"
  ],
  "author": "Vincent Ramdhanie",
  "license": "MIT"
}
```
Notice that I accepted the defaults wherever. As we proceed I will modify this file
with the details.

#### README.md
Add a new file named _README.md_. This file will describe your project for persons
wishing to use your package in their own project.

```bash
touch README.md
```

#### Setup Babel
Babel will be used to transpile ECMAScript 6 code into ECMAScript 5.

```bash
npm install babel-cli babel-preset-latest --save-dev
```

The `--save-dev` option adds babel as a dependency in the _package.json_ file.

Next add an npm script to the _package.json_ file.

```javascript
"build":"babel src -d build"
```
This builds everything in the __src__ directory and places the output in the __build__ directory.

#### Configure Babel
Add a new top level property to the _package.json_ file.

```javascript
"babel": {
    "presets": ["latest"]
}
```

#### Initialize Git
Create a git repository and a _.gitignore_ file.

```bash
git init
touch .gitignore
```

Edit the .gitignore file and add an entry for the __node_modules__ directory.

```bash
node_modules/
```
You may include any other file that you wish git to ignore.




### Write Code
Describe the basic code

### Watch
Setup watching to make the build process better

### Testing
Describe test setup with Jest

### Linking
How to test your package locally

### Documentation
Write documentation for your package

### Publish
Push your package to the npm repository

### Update
How to update your package after publication


```javascript
let a = ['twenty']
```
That was some code.
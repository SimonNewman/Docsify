# Gulp

Gulp.js is a build system, meaning that you can use it to automate common tasks in the development of a website. It’s built on Node.js, and both the Gulp source and your Gulp file, where you define tasks, are written in JavaScript.

> Common tasks include compiling SCSS code, auto prefixing and creating source maps.

## Prerequisites

[Node.js](development/node.md) should be installed.

## Installation

If Gulp isn’t installed on your system, carry out the following steps:

1.	Open a terminal window such as **PowerShell**
2.	Install Gulp globally by running `npm install -g gulp`
3.	Now the `gulp` command will be available to use

## Creating a new project

A gulp project requires a **package.json** and **gulpfile.js** file. **package.json** will contain all the dependencies required by the project. **gulpfile.js** will contain the actual code to run your tasks.

Create a **package.json**;

1.	Open a terminal in the project directory
2.	Run `npm init`
3.	This will start an interactive configuration
4.	Follow the prompts to set up your file
5.	Make sure the entry point is **gulpfile.js**

Here is an example **package.json**

```json
{
  "name": "my-new-project",
  "version": "1.0.0",
  "description": "",
  "main": "gulpfile.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "Formation Media",
  "license": "ISC"
}
```

## Installing packages

You can install any package from [npmjs.com](https://www.npmjs.com/) by following the instructions. This will automatically add the dependency to the **package.json** file.

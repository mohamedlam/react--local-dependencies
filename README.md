# Project usage Proof of Concept

A Proof of concept of using an additional project (Local) as dependency to separate logic. 

It also helps you write true re-usable projects or sub-modules.

the difference between a project as a dependency and sub-module, is that the sub-module is inside the main project.

## Running the app

```
npm install
npm start
```

If you run npm 3+, you need to remove the `preinstall` script in package.json


## Creating new project as a dependency

* Create a new folder for your dependency, such as `../new_dependency` (anything else)
* Create a `package.json` file for it, along with the usual `README.md`
* Adds its dependencies in its own `package.json`
* Install this local package in your top level project (Ex: project_a) using: `npm install --save ../new_dependency`.
* then import what ever you need from it.

Optional package :

* Install esm package which allows you to use ES6 modules in node (Ex: use import/export) `npm esm install`. 
* Then, you need to require this package when starting your server with node, for example if your node server runs index.js file, you would use the command `node -r esm index.js`.

## Updating a local project/dependency

* Update whatever you want in your project (including dependencies)
* change your project/dependency version in its `package.json` (important)
* then run `npm update` or `npm update my-module`
 
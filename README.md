# Webpack basic site template

Basic website template on Webpack to be used for regular websites rather than web applications. Supports: compile Sass to standalone css file, ES6, Vue.js with components, hot reload for JS & CSS, Autoprefixer, disabled processing images.

## Purpose

There are several Webpack/Vue.js templates like [this](https://github.com/vuejs-templates/webpack) and [this](https://github.com/vuejs-templates/webpack-simple), but they are mostly focused on web applications. They expect styles to be in components, process images in CSS, everything is wrapped in Vue and Webpack bundle.

For a simple website, you want content as standard HTML for search engines to index it. Sometimes you figure out you don't need Vue at all, so you want to easily remove it. You want stylesheets outside of webpack so they can be easily linked without Javascript if needed.

Basically what I was looking for was something like good old Grunt / Gulp build process for SCSS, but on Webpack handling JS dependencies if needed, with the basic tools like browser refresh and autoprefixer. I haven't found anything simple enough around, so I created my own.

## Features

- very lightweight
- compiles SCSS
- bundles JS dependencies through Webpack
- ES6 syntax through Babel
- Vue.js with loader for components (both can be easily removed if not used)
- hot reload for both CSS and JS changes
- autoprefixer
- no image manipulation (keeps images untouched)

## Structure

```
 .
├── dist/             // generated folder of compiled assets
│   └── app.css       // compiled stylesheet
│   └── app.js        // compiled webpack javascript bundle
│
├── src/              // JS & SCSS source files
│   └── js/           // javascript files, components, libraries ..
│      ..	
│   └── scss/         // scss files
│      ..	
│   └── app.js        // bootstrap for JS
│   └── app.scss      // bootstrap for SCSS
│
├── img/              // folder to hold unprocessed images, can be renamed or deleted
│      ..	
│
├── index.html        // sample index file 
..
..                    // any other folders, files or whatever you need
..

```


## Build Setup

``` bash
# install dependencies (use 'npm install' instead if not using Yarn)
yarn install

# serve with hot reload at localhost:8080
npm run watch

# build for production with minification
npm run prod
```

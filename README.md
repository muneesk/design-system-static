# Design System

> A Design System Starter Kit for  AEM Static web development.

## Features / Use Cases
This Design System provides a simple way of setting up a modern web development environment.
Here is a list of the current features:

- Copy HTML files from `src` to `dist` directory
- Compile Pug template files (`.pug`) from `src` to HTML files and put them inside `dist` directory
- Compile CSS preprocessor code (Sass/SCSS, Less, Stylus) to CSS
- Autoprefix and minify CSS and put it inside `dist` directory
- Compile ES6+ to ES5, concatenate JS files and minify code
- Compress and copy images into `dist` directory
- Copy dependencies specified in `package.json` from `src/node_modules` directory into `node_modules` folder inside `dist` directory
- Import dependencies into your application with ES6 modules
- Spin up local dev server at `http://localhost:3000` including auto-reloading

## Requirements
This should be installed on your computer in order to get up and running:

- [Node.js](https://nodejs.org/en/) (Required node version is >= 10.0)
- [Gulp 4](https://gulpjs.com/)
## Getting Started
In order to get started, make sure you are meeting all requirements listed above.
Then, just go ahead and download the Design System. For this, you can choose between the following options:
### What kinds of build scripts does the Design System offer?
The Design System offers two different build scripts:

1. `npm run build`: This is used to build all files and run all tasks without serving a development server and watching for changes.
2. `npm start`: This is the normal development script used to build all files and run all tasks, but also to serve a development server and watch for changes.

### How can I use another CSS preprocessor than Sass?
In case you prefer to use one of the other supported CSS preprocessors over Sass, you can simply create a new directory `src/assets/css-processor-name` which is where all your CSS preprocessor files have to be placed.
After you have moved all your code to the new folder, just make sure to delete the `sass` directory and everything should work as expected.

Here's a list of the currently supported CSS preprocessors and the corresponding directory names:

- Sass (`src/assets/sass`)
- SCSS (`src/assets/scss`)
- Less (`src/assets/less`)
- Stylus (`src/assets/stylus`)

### How can I specify for which browsers CSS code should be autoprefixed?
The recommended way of specifying which browsers should be targeted by the CSS autoprefixer is to add a `browserslist` key to `package.json`:

```json
{
  "browserslist": [
    "last 3 versions",
    "> 0.5%"
  ]
}
```

You can find [more information on that topic](https://github.com/postcss/autoprefixer#browsers) in the README file of the employed [PostCSS plugin](https://github.com/postcss/autoprefixer).

### What types of images are supported?
The following types of images are currently supported:

- PNG
- JPG / JPEG
- GIF
- SVG
- ICO (not compressed)

### How can I specify dependencies which are then copied to the `dist` folder?
You don't need to specify your dependencies anywhere else than in your `package.json` file.
Just install your dependencies via npm and all your dependencies get automatically loaded and copied into the `dist` folder.

### How can I load dependencies inside my application?
ES6 modules are supported by this Design System.
Just install your dependencies and import them like so:

```js
import axios from 'axios';
```
## License

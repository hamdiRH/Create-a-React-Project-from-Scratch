Step 1: Initialize NPM (Node Package Manager)
mkdir new-react-app
cd new-react-app
npm init --y

Step 2: Install React, Webpack, and Babel
npm install --save-dev webpack webpack-dev-server html-webpack-plugin @babel/core babel-loader @babel/preset-env @babel/preset-react 

Step 3: Create the files
touch webpack.config.js
mkdir src
cd src
touch index.js
touch index.html

Step 4: Create NPM run scripts
  // package.json
    ...
  "scripts": {
    "start": "webpack-dev-server --open",
    "build": "webpack"
  },
  ...
  
Here's what each package does:
react: UI library for creating modular components
react-dom: enables us to render the React within the browser DOM
webpack: bundler that converts your source code into production-ready output
webpack-dev-server: transforms our source code and serves it on a web server as we develop it continuously. This helps use see the output of your code in the browser.
html-webpack-plugin: an extension to webpack that adds the basic index html file
@babel/core: a JavaScript transpiler to converts modern JavaScript into a production-ready version that's compatible with all browsers.
babel-loader: connects Babel to webpack's build process
@babel/preset-env: group of commonly used Babel plugins bundled into a preset that converts modern JavaScript features into widely compatible syntax
@babel/preset-react: React-specific Babel plugins that convert JSX syntax into plain old JavaScript that browsers can understand

Quick note: --save-dev flag is for partitioning the dependencies into development-specific dependencies, so that they are not included in the production JavaScript bundle

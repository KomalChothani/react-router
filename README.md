# react-router

<!-- 
    Steps to setup the React project from scratch
    https://www.tutorialspoint.com/reactjs/reactjs_environment_setup.htm
 -->

1. Open command prompt from Root directory/folder and do 
    npm init

2. install react & react-dom in root folder
    npm install react --save
    npm install react-dom --save

3. install webpack, webpack-dev-server & webpack-cli in root folder
    npm install webpack --save
    npm install webpack-dev-server --save
    npm install webpack-cli --save

4. install babel
    npm install babel-core --save-dev
    npm install babel-loader --save-dev
    npm install babel-preset-env --save-dev
    npm install babel-preset-react --save-dev
    npm install html-webpack-plugin --save-dev

    npm i @babel/preset-typescript
    npm i @babel/preset-react
    npm i @babel/preset-env
    npm i @babel/plugin-transform-runtime

5. create following files
    Inside root folder
        .babelrc
        webpack.config.js
    Inside src folder
        index.html
        index.js
        App.js

---------------------------------------------------------------

*  What is webpack?
https://levelup.gitconnected.com/what-is-webpack-4fdb624597ae
https://webpack.js.org/concepts/

-> Webpack is a static module bundler for JavaScript applications.

-> it takes all the code from your application and makes it usable in a web browser.

-> Modules are reusable chunks of code built from your app’s    
    JavaScript,
    node_modules,
    images, and 
    the CSS styles 
which are packaged to be easily used in your website.

-> Webpack separates the code based on how it is used in your app, and with this modular breakdown of responsibilities, it becomes much easier to manage, debug, verify, and test your code.

-> When Webpack processes your application, it builds a dependency graph
    -> Any time one file depends on another, webpack treats this as a dependency.
    
    -> This allows webpack to take non-code assets, such as images or web fonts, and also provide them as dependencies for your application.

    -> When webpack processes your application, it starts from a list of modules defined on the command line or in its configuration file.
    
    -> Starting from these entry points, webpack recursively builds a dependency graph that includes every module your application needs, then bundles all of those modules into a small number of bundles - often, only one - to be loaded by the browser.

-> Webpack can be broken down into these 5 principals:
    Entry
    Output
    Loaders
    Plugins
    Mode

-> Entry:
    -> Entry is the entry point for the application.

    -> It is the first module (JavaScript file)that Webpack will process to build out the full dependency graph.

    -> It will look at the files that are imported into the entry, and these are added to the dependency graph. It then continues to walk through all the imported files until it has accounted for all the code needed to run the applications.

    -> Webpack figures out which other modules depend on the entry point, both directly and indirectly.
    
    -> The default entry point in modern JavaScript applications is ./src/index.js, but it can be set to any file of your choosing.

-> Output:
    -> Output point is where the files are to be written on disk with the name of the files. The main output file is written as ./dist/main.js.

-> Loader
    -> webpack only understands JavaScript and JSON files.
    
    -> Loaders allow webpack to process other types of files and convert them into valid modules that can be consumed by your application and added to the dependency graph.

    -> loaders have two properties in your webpack configuration:

        -> The test property identifies which file or files should be transformed.

        -> The use property indicates which loader should be used to do the transforming.

-> Plugines
    -> While loaders are used to transform certain types of modules, plugins can be used to perform a wider range of tasks like 
        -> bundle optimization,
        -> asset management and 
        -> injection of environment variables.

    -> It can also be used to extract a stylesheet or create an index.html file for a single-page web application.

-> Mode
    -> The mode parameters should either development, production, or none. If mode is not specified, then Webpack automatically defaults to production.

--------------------------------------------------------------

* Use of .babelrc file

-> Babel is used to convert ECMAScript 2015+ code into a backwards compatible version of JavaScript in current and older browsers or environments.

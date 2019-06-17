# Node

Node.js runs JavaScript code. This means that millions of frontend developers that already use JavaScript in the browser are able to run the server-side code and frontend-side code using the same programming language without the need to learn a completely different tool.

For us, that means we can run javascript on our local computers without needing to rely on the browser and eventually we can build web servers with javascript!

## Installation

Let's install node together.  In your terminal, run the following command
```
brew install node
```

Then we can check what version of node we have downloaded with
```
node -v
```

For windows users or those not using `brew`, follow [install steps here](https://nodejs.org/en/)

## Node JS REPL

With Node, we can enter a javascript REPL environment, similar to our browser console.

To do this, we simply run `node` in the terminal.
Notice how now our terminal starts with `>`.

We are now in a javascript REPL environment so commands like `ls` or `cd` will not work.  But commands like `const name = 'Mike'` will.

To exit the REPL we can type `.exit` or use `ctrl + c`.

```
$ node
> 1 + 1
2
> .exit
$
```

## Running JS files with Node

We have a javascript file located at [js/practice.js](js/practice.js).
We can execute that file with node by running `node js/practice.js` in the terminal.

## Exporting JS files with Node

With node, we are able to export data from one file into another file.  HOORAY!  What an exciting feature.  We often call the file that exports data into another file a module.  We can include many modules into a JS file.  Let's try doing this together.

We have an example of a module in [js/person.js](js/person.js).
We are exporting the data from this file into a file named [js/introduction.js](js/introduction.js)].
These names are not important and we can name the files anything we want.
Together, let's review the files and we will see how exporting and requiring a file works in JS.

## NPM (node package manager)

A node package is one or more modules grouped together.  To help us manage our packages node includes a package manager named NPM.  We can use it to install packages globally throughout our whole computer or locally to individual projects.  

### Cool ASCII Faces

To install the package globally we can do
```
npm install cool-ascii-faces --global
```
And then we can use the command line commands like:
```
cool-face
```

If we want to use it in our own JS file then we need to initiate our folder to use NPM and then install the package to that project.
```
npm init

npm install cool-ascii-faces
```

Notice the `package.json` file that NPM created for us and how it includes the dependency for cool-ascii-faces.

Now let's look at and run our [js/funnyFaces.js](js/funnyFaces.js) file to use the package in our JS file.

## NPM Scripts

We can add scripts to the `package.json` and NPM will run them for us.  A common script to add is `start` which should start your application.  Let's make the `start` script run `node js/funnyFaces.js` for us so we can use the command `npm start` instead of having to type out `node js/funnyFaces.js`.

## node_modules

You may have noticed that NPM also created a `node_modules` folder which includes all the modules we have included in our application.  BEWARE! It is extremely large and rarely, if ever, should you be opening it.

![node](https://pbs.twimg.com/media/DEIV_1XWsAAlY29.jpg)

## Additional Resources

- https://nodesource.com/blog/the-basics-of-package-json-in-node-js-and-npm/
- https://www.youtube.com/watch?v=w-7RQ46RgxU&list=PL4cUxeGkcC9gcy9lrvMJ75z9maRw4byYp
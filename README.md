# What is ReactJS?
ReactJS is an open-source, component based front end library responsible only for the view layer of the application. It is maintained by Facebook.

React is a JavaScript library for building composable user interfaces. This means that we can build a user interface by composing items called components. A component is an element that contributes to building a user interface. It could be a textbox, a button, a whole form, a group of other components, and so on. Even the entire application's user interface is a component. So, React encourages the creation of components to build a user interface; it's even better if these components are reusable.

Since the library deals with user interfaces, you may wonder which presentational design patterns React was inspired by: Model-ViewController, Model-View-Presenter, Model-View-ViewModel, or something else. React is not bound to a specific presentational pattern. React implements the View part of the most common patterns, leaving developers free to choose the best approach to implement the model, the presenter, and everything else they need to build their application. This
aspect is important, since it allows us to classify it as a library, not as a framework; therefore, comparisons with frameworks such as Angular may throw up some inconsistencies.

The most powerful thing about React is that can be used in the client, server, mobile applications, and even VR applications.

Companies such as Airbnb, Microsoft, Netflix, Disney, Dropbox, Twitter, PayPal, Salesforce, Tesla, and Uber are extensively using React in their projects.

# React Developer Tools
There are several developer tools that can be installed as browser extensions or addons that you may find useful as well:
- i) **react-detector** - react-detector is a Chrome extension that lets you know which websites are using
React and which are not.
- ii) **show-me-the-react** - This is another tool, available for Firefox and Chrome, that detects React as you
browse the internet.
- iii) **React developer tools** - This is a plugin that can extend the functionality of the browser’s developer tools.
It creates a new tab in the developer tools where you can view React elements. If you prefer Chrome, you can install it as an extension; you can also install it as an add-on for Firefox.

# Installation of React
Fortunately, we can use create-react-app, a command-line interface (CLI) tool that allows us to set up a React-based application without needing to configure any of the aforementioned tools. It is based on Node.js and provides commands to set up and modify a React application in an immediate way.

In order to install create-react-app, you need Node.js installed on your machine. You can install the CLI by typing the following command in a console window: 
```npm install -g create-react-app```

After installation, you can verify whether it is properly installed by typing the following command:
```create-react-app --version```
If all is OK, the installed version of create-react-app will be shown.

#Creating Your First React Application
Let's create our first React application by typing the following command in a console window:
```create-react-app hello-react```

This command tells create-react-app to set up all of the prerequisites for a React-based application named hello-react. The creation process may take several minutes, since it has to download the npm packages needed for the project.

Let's take a look at the files generated by create-react-app, so that we can get an understanding of the structure of a React-based application. We will find these files and folders inside of the HELLO-REACT folder:
> In the root folder, we can see a README.md file, the package.json file, and
the .gitignore file.
- **README.md** :  The README document contains references to all you need to start building a React-based application. It is written in Markdown format, and you can integrate or overwrite it with your own documentation.
- **package.json** : The package.json file contains information about the project, such as the name, the version, and so on, and references to all the npm packages used by the current project. This is a Node.js asset that allows you to download
the required packages when copying the project to another machine. It also contains the definitions of scripts that allow us to manage the project itself.
- **.gitignore** : The .gitignore file is a hidden file in Unix-based systems, and it allows us to track which file(s) to ignore when using Git as a version control system. The create-react-app tool added this file because nowadays, it is essential to have a project under version control. It suggests Git, since it is one of the most popular version control systems.
> The public folder contains the static parts of our application:
- **favicon** : This is the icon shown in the browser's address bar and is used for bookmarks.
- **index.html:** : This is the HTML page containing the reference to our React code and providing a context to React rendering.
- **manifest.json:** : This is a configuration file containing metadata according to the Progressive Web Apps (PWA) criteria.

In particular, the index.html file is the starting point of our application. Let'stake a look at it so that we can understand what's special about it:
```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1,
shrink-to-fit=no">
<meta name="theme-color" content="#000000">
<link rel="manifest" href="%PUBLIC_URL%/manifest.json">
...
<title>React App</title>
</head>
<body>
<noscript>
You need to enable JavaScript to run this app.
</noscript>
<div id="root"></div>
...
</html>
```
As we can see, it is a standard HTML page; however, a few things should be noted. First of all, we see a link to the manifest.json file:
```html 
<link rel="manifest" href="%PUBLIC_URL%/manifest.json">
```
This manifest contains metadata for configuring our app as a PWA.

The second thing we notice is the %PUBLIC_URL% placeholder in both link references:
```html
<link rel="manifest" href="%PUBLIC_URL%/manifest.json">
<link rel="shortcut icon" href="%PUBLIC_URL%/favicon.ico">
```
This placeholder will be replaced with the actual URL of the public folder during the build process.

```html 
<div id="root"></div>
```
The body of the HTML page contains an empty div with a root identifier. This is an important item for the correct setup of our React application

The build process will be responsible for adding the required scripts to the body. We can add any other required items to the HTML page, such as meta tags, web fonts, and so on. However, remember that files referenced inside the HTML markup should be put in the public folder. The node_modules folder contains the npm packages used by the project. Usually, you don't need to directly manage these files.

> The most important folder for developing our application is the src folder. It contains the basic files, with the code that we can modify for our purposes. In particular, we will find the following files:
- **index.js** : Contains the starting point of our application.
- **index.css** : Stores the base styling for our application.
- **App.js** : Contains the definition of the main component of the sample application.
- **App.css** : Contains the styling of the App component.
- **logo.svg** : This is the React logo.
- **App.test.js** : Stores the basic unit test involving the App component.
- **registerServiceWorker.js** : Contains the code to register the service worker in order to allow offline behavior, as per the PWA requirements

>The first command we will cover is ```npm start```. This command starts a development web server accepting requests at ```http://localhost:3000```.

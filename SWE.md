# Full Stack Software Engineering

### Author: [Weizhi Du](https://weizhi-du.github.io)

#### *Computer Science and Financial Engineering Student @ WashU*


<br/>

Everyone can be a software engineer, really.

This guide is inspired by and based on the *IBM Full Stack Software Developer* series. Reading this guide is merely a starting point (0 to 1). What makes 1 to N is your dedication on practicing and building your own projects. There should be no prior experience required for Modules 1-4. From Module 5 and onwards, I would recommend the knowledge of at least one programming language, or one introductory course like CSE247. Also, feel free to skip the parts you are already familiar with. Pull out your command line and IDE, and happy coding!

## Content

[**1. An Overview of Software Engineering**](#1-an-overview-of-software-engineering)

[**2. Introduction to Cloud Computing**](#2-introduction-to-cloud-computing)

[**3. HTML, CSS, and JavaScript**](#3-html-css-and-javascript)

[**4. Git and GitHub**](#4-git-and-github)

[**5. React and the Front-End**](#5-react-and-the-front-end)

[**6. Node.js and Express for Back-End**](#6-nodejs-and-express-for-back-end)

[**7. Python**](#7-python)

# 1. An Overview of Software Engineering


## Basic Terminology

> There will be a lot of terms in this guide. I will try to make them easy. They can be a little bit annoying but they truly make better practices :) If you are still confused, ask Google or GPT to give some illustrative explanations.

- **SDLC**: Software Development Life Cycle, containing Planning, Analysis, Design, Implementation, Testing, and Maintenance.
- **Agile**: An iterative approach to software development that emphasizes collaboration, flexibility, and continuous improvement.
- **Front-end**: The part of the software that runs on the client's browser. Basically *CSE204* if you are a WashU student. May contain HTML, CSS, JavaScript, and libraries/frameworks like React.
Specifically, HTML is to build the structure of the page, CSS is to style the page, and JavaScript is to add interactivity.
- **Back-end**: The part of the software that runs on the server. Basically *CSE330* and *CSE427* if you are a WashU student. Covers logic, functions, and databases.
- **CI/CD**: Continuous Integration/Continuous Deployment, a practice that allows you to test and deploy code more frequently. *CI:* Automatically build and test code changes. *CD:* Automatically deploy code changes.


# 2. Introduction to Cloud Computing


## 2.1 Cloud Computing Concepts

- **Cloud Computing**: The on-demand availability of computer system resources, especially data storage and computing power, without direct active management by the user. AWS, Azure, and Google Cloud are the leading cloud service providers.
There are three types of cloud services:
    - **Infrastructure as a Service (IaaS)**: Provides virtual machines, storage, and networking.
        - Physical data centers: do not interact with the user, but provided as a service.
        - Compute, Network, Storage: Services to provide scalable computing power, network, and object/file/block storage.
        
    - **Platform as a Service (PaaS)**: Provides a platform for building and deploying applications, including databases, OS, development tools, analytics, etc.
        - Platform to develop, deploy, and run.
    - **Software as a Service (SaaS)**: Provides software applications. Apps and data.
        - Users can run apps with minimal setup.
- **Example: IoT, AI, and Cloud**: Three way relationship. IoT provides data (and behave based on AI response), AI acts on data, and cloud provides scalable storage and computing power.
- **Four Types of Cloud Computing**:
    - **Public Cloud**: Shared infrastructure, pay-as-you-go. Like paying for electricity.
    - **Private Cloud**: Dedicated infrastructure, on-premises. Like having your own electricity generator. However, users can use Virtual Private Cloud (VPC) to connect to a private part of the public cloud.
    - **Community Cloud**: Shared infrastructure, but limited to a specific group.
    - **Hybrid Cloud**: Combination of public and private clouds. Like having your own electricity generator and buying electricity from the public grid. They are interoperable (understand each other's APIs), scalable, and portable.


## 2.2 Cloud Infrastructure

- **Virtualization**: The process of creating a virtual (rather than physical) version of something, such as a hardware device, operating system, or storage.
    - **Hypervisor**: Software that allows multiple operating systems to run on a single physical machine. Each OS runs in its own virtual machine.
    - **Virtual Machine**: A virtualized computing resource that runs an operating system.
- **Containers**: A standard unit of software that packages code and dependencies together. It allows you to run an application in a lightweight environment.
- **Cloud Storage**: A cloud-based storage system that allows you to store and retrieve data from the cloud. IOPS is the number of input/output operations per second, a measure of the storage's performance.
    - **File Storage**: A storage system that allows you to store and retrieve files from the cloud. It is attached via ethernet connection. Good for file sharing.
    - **Block Storage**: A storage system that allows you to store and retrieve blocks of data from the cloud. It blocks data into fixed-size units and stores each block separately. It is fast, expensive, consistent, secure, and extremely resilient to failure.
    - **Object Storage**: A storage system that allows you to store and retrieve static objects from the cloud. It is good for large unstructured data. It is effectively infinite



## 2.3 Some Trends and Practices

- **Hybrid Multi-Cloud**: A strategy that involves using multiple cloud providers to meet specific needs. It allows you to use the best cloud for the best job while not being locked in.
- **Microservices**: A software design pattern that allows you to break down a large application into smaller, independent services. Each service can be developed, deployed, and scaled independently. Multiple developers can work on different services simultaneously.
- **Serverless Computing**: A cloud computing model that allows you to run code without provisioning or managing servers. It is a type of event-driven computing. Users only pay for the compute time, and code is executed as individual units.
- **DevOps**: A practice that combines software development and operations. It is a way to improve collaboration between developers and operations teams to deliver better software continuously.
- **Cloud Native**: A software design pattern that allows you to build and deploy applications that are optimized for the cloud. It is a way to containerize microservices to improve scalability, resilience, and performance.


## 2.4 Cloud Security

- **Basics**:
    - **Principle of Least Privilege**: Only give the minimum permissions needed to do the job.
    - **User Access Level**: Users can be classified into different levels based on their access rights.
    - **Identity and Access Management (IAM)**: A system that allows you to manage and authenticate user identities and access rights (administrators, developers, users).
    - **Standard Password Policy**: A policy that requires users to set complex password and change their passwords regularly.
    - **Identity provider standards (SAML, OpenID)**: Protocols to securely exchange authentication and authorization data between two parties.
        - **Security Assertion Markup Language (SAML)**: Allows SSO (Single Sign-On) and allows users to access multiple applications with the same credentials.
        - **OpenID**: Allows users to obtain an ID token from an OpenID provider.
- **Cloud Encryption**: scrambling data to make it unreadable to unauthorized users.
- **Cloud Monitoring**: Set alarms for unusual activities, make logs to track the usage, and visualize performance data.



# 3. HTML, CSS, and JavaScript

> Hopefully things get a little bit exciting here. This only includes the basics. You may need a cheat sheet for more features.

## 3.1 HTML (Hypertext Markup Language) and a little bit of DOM (Document Object Model)

**A simple HTML example**:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>My First HTML Page</title>
    </head>
    <body>
        <h1>Hello, World!</h1>
        <p>This is a paragraph.</p>
        <!-- This is a comment -->
    </body>
</html>
```

SEO uses keywords provided by meta tags to optimize the search engine results:

```html
<meta name="description" content="This is a description of my page">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="author" content="Weizhi Du">
```

Every HTML document is represented by a document object. The DOM tree accessors are HTML document APIs that provide access to all HTML elements in the document.

HTML document API - DOM tree accessors:

- **head**: Return the head element.
- **title**: Sets or return the title of the document.
- **images**: Return an HTMLCollection of img elements in the document.
- **lastModified**: Return the last modified date of the document.
- **scripts**: Return an HTMLCollection of script elements in the document.

HTML document API - DOM tree methods:

- **getElementById(id)**: Return the first element with the specified id.
- **getElementsByTagName(tagName)**: Return an HTMLCollection of elements with the specified tag name.
- **open()**: Open an output stream to collect output from document.write().
- **write()**: Write Javascript code to a document.
- **close()**: Close the output stream.

Not all HTML/CSS features are supported in all browsers. Use caniuse.com to check the support.

The input field allows users to enter data (can be validated on the client side). These include text, password, email, number, date, time, etc.

```html
<input type="text" name="username" placeholder="Enter your username" required>
```

## 3.2 CSS (Cascading Style Sheets)

Inline styles:

```html
<p style="color: red; font-size: 20px;">This is a paragraph.</p>
```

Internal styles:

```html
<style>
    p { color: red; font-size: 20px; }
</style>
```

External styles:

```html
<head>
    <link rel="stylesheet" type="text/css" href="styles.css">
</head>
```

Utility-first frameworks:
- Tailwind CSS
help create responsive websites. For example:

```html
<img class="w-16 md:w-32 lg:w-64" src="...">
```

Component frameworks:
- Bootstrap

```html
<button class="link-danger">Danger Zone</button>
```


## 3.3 JavaScript

### 3.3.1 Variables and Data Types

> Note: Use `let` or `var`? `let` is a block-scoped variable, while `var` is a function-scoped variable. It's a good practice to use `let` for better scope control and fewer bugs.

**Primitive and wrapper objects**:

```js
typeof "abc"; // "string"
typeof String("abc"); // "string"
typeof new String("abc"); // "object"
typeof (new String("abc")).valueOf(); // "string"
```

**Arrays**:

```js
numArray = new array(0,1,2,3,4,5);
numArray.length; // 6

colors = ["red", "green", "blue"];
colors.length; // 3
colors[0]; // "red"
colors[1] = "yellow"; // ["red", "yellow", "blue"]
colors.push("purple"); // ["red", "yellow", "blue", "purple"]
colors.pop(); // ["red", "yellow", "blue"]
```

> Note: Arrays are zero-indexed.

**Date objects** (represented in YYYY-MM-DD HH:MM:SS UT):

```js
let date = new Date();
date.getFullYear(); // 2024
date.getMonth(); // 0 (January)
date.getDate(); // 15
date.getDay(); // 4 (Thursday)

let date2 = new Date("2024-01-15 12:00:00");
let date3 = new Date(2024, 0, 15);
```

> Note: JavaScript uses 0-based indexing for months. January is 0, February is 1, etc.


### 3.3.2 Control and Loops

**The `if` statement**:

```js
let x = 10;
if (x > 0) {
    console.log("x is positive");
} else if (x < 0) {
    console.log("x is negative");
} else {
    console.log("x is zero");
}
```

**The `switch` statement**:

```js
let x = 10;
switch (x) {
    case 10:
        console.log("x is 10");
        break;
    case 20:
        console.log("x is 20");
        break;
    default:
        console.log("x is not 10 or 20");
}
```

**The `for` loop**:

```js
for (let i = 0; i < 10; i++) {
    console.log(i);
}
```

**The `while` loop**:

```js
let i = 0;
while (i < 10) {
    console.log(i);
}
```

> Looks familiar, right? The more programming languages you know, the lower the learning curve is.


### 3.3.3 Functions

**Function**:

```js
function add(a, b) {
    return a + b;
}

let x = add(1, 2); // x = 3
x = add(3, 4); // x = 7
x = add("hello", "world"); // x = "helloworld"
```

**ES6 Function**:

```js
let myPrint = (input) => {
    console.log(input);
}

myPrint("Hello, world!"); // "Hello, world!"
```



**Create custom objects**:

```js
function Person(name, age) {
    this.name = name;
    this.age = age;
    this.greet = function() {
        return name + " says hello!";
    }
}

let person = new Person("John", 20);
alert(person.greet()); // "John says hello!"
```

> Objects can be created in functions (there are also other ways).

**Prototype**:

```js
function Person(name, age) {
    this.name = name;
    this.age = age;
}

Person.prototype.greet = function() {
    return this.name + " says hello!";
}
```

Prototype is a property of functions that allows you to add methods to objects.

**Self-executing functions**:

These are functions that are executed immediately after they are defined. Can be used to initialize data or declare DOM elements on the page.

```js
(function() {
    console.log("This is a self-executing function.");
})();
```

### 3.3.4 JavaScript API

**Document**

```js
// pass in id to retrieve one specific element
document.getElementById("myElement");

// pass in tag name to retrieve all elements with that tag name
document.getElementsByTagName("p");

// create a new element. Can be used to place to a location
document.createEvent("name");

// add a child element to a parent element
parentNode.appendChild(childNode);
```

**Element**

```js
// get/set the content within the element. Return all child elements as a text string
element.innerHTML
// get/set the CSS style of the element
element.style
element.style.color = "red";

// set an attribute of the element
element.setAttribute("style", "color: red;");

// get an attribute of the element
element.getAttribute("style");

// add an event listener to the element
element.addEventListener("click", function() {
    console.log("The button was clicked!");
});
```

**Window**

```js
// open a new window
window.open("https://www.google.com", "_blank");

// run a function when the page is loaded
window.onload

// scroll to a specific position
window.scrollTo(0, 100);
```

**RESTful API**:

Representational State Transfer (REST) APIs follow the CURD operations: *Create (**POST**), Update (**PUT**), Read (**GET**), Delete (**DELETE**)*.


### 3.3.5 Client-Side JavaScript

We can use the `<script>` tag to include JavaScript code in our HTML:

```html
<script src="script.js"></script>
```

Or directly write JavaScript code in the `<script>` tag:

```html
<script>
    console.log("Hello, world!");
</script>
```

`noscript` tag is used to provide alternative content for users who have disabled JavaScript:

```html
<noscript>
    Please enable JavaScript to view this content.
</noscript>
```

Scripts can be tied to events. For example, the `onclick` event is triggered when the user clicks on an element:

```html
<button type="button" onclick="showAnswers()">Show Solutions</button>
```

```js
function showAnswers() {
    alert("Answer: C");
}
```

Here is a little bit more DOM. It's a browser-based interface for applications and scripts. JavaScript uses DOM to access and modify the content of the page.



# 4. Git and GitHub

> For the knowledge of Git, I highly recommend you to complete the [this Git tutorial with exercises](https://learngitbranching.js.org/) (that was how I learned it). What I have here in the notes are just the basics.

## 4.1 Basic Terms

- **Git and GitHub**: Git is a distributed version control system, while GitHub is a web-based Git repository hosting service.
- **GitLab**: A DevOps platform. It provides access to Git repositories, CI/CD, and other tools.
- **SSH Protocol**: Secure Shell Protocol, a protocol for secure remote login from one computer to another.
- **Repository**: A collection of files and folders.
- **Fork**: A copy of a repository.
- **Pull Request**: A request to merge a branch into another branch.
- **Commit**: A snapshot of the repository at a specific point in time.
- **Branch**: A version of the repository that can be different from the main branch.
- **Merge**: Combine changes from one branch into another.
- **Clone**: A local copy of a repository.
- **Push**: A process of sending a branch to a remote repository.
- **Pull**: A process of receiving a branch from a remote repository.


## 4.2 Git Workflow

**Branches**:

Branches store all files. `Main` branch stores the production-ready code. You can create a new branch for any planned changes.


**Workflow**:

1. Clone the repository to local.
2. Create a new branch for any planned changes.
3. Commit the changes to the branch.
4. Push the branch to the remote repository and create a pull request.
5. Lead developers review, approve, and merge the pull request to the main branch.
6. Other developers can pull the latest changes from the main branch to local.


**Git Commands**:

Initialize a new repository. Set up necessary files and directories:
```bash
git init
```

Add files to the staging area from the working directory:
```bash
git add <file_name>
```

Commit the changes. Save the changes with a message:
```bash
git commit -m "commit_message"
```

Browse the repository history:
```bash
git log
```

Create a new branch to work on:
```bash
git branch <branch_name>
```

Switch between existing branches:
```bash
git checkout <branch_name>
```

View the status of all changes in relation to the repository:
```bash
git status
```

Merge the feature branch into the main branch:
```bash
git merge <branch_name>
```

**Clone vs. Fork**:

- **Clone**: A local copy of a repository.
- **Fork**: A remote copy of a repository.


# 5. React and the Front-End

> Why? React is the most used framework for building UIs. It uses reusable components to build complex web applications.

## 5.1 React Basics

### 5.1.1 The build tools

- **Create React App (CRA)**: A tool to create a new React application. Will lead to large bundle sizes.
```bash
npx create-react-app my-app
```

- **Vite**: A build tool that is faster and more efficient than Create React App.
```bash
npm create vite@latest
```

### 5.1.2 React Folder Structure

- **node_modules**: The dependencies of the application through npm and yarn.
- **public**: Static assets like HTML files, images, and favicon.
- **src**: The source code for React application.
    - **src/main.jsx**: The entry point of the React application.
    - **src/App.jsx**: The root component of the React application.
- **package.json**: Metadata, scripts for running, building, and testing the application.
- **index.html**: Entry point for web application.


### 5.1.3 ES6 Features

1. **`let` and `const`**: While `var` is in the global scope, `let` and `const` are in the block scope.
2. **Arrow Functions**: a clean way to write functions.
```js
function add(a, b) {
    return a + b;
}

// is equivalent to
const add = (a, b) => a + b;

// is equivalent to
const add = (a, b) => {
    return a + b;
}
```

3. **Promises**: A clean way to handle asynchronous operations.
Resolve: action is fulfilled.
Reject: action is rejected.
```js
const myPromise = new Promise((resolve, reject) => {
    setTimeout(() => {
        if (Math.random() > 0.5) {
            resolve("Success!");
        } else {
            reject("Failure!");
        }
    }, 1000);
});

myPromise.then((result) => {
    console.log(result); // Run on success
}).catch((error) => {
    console.log(error); // Run on failure
});
```

4. **Classes**: 

```js
class Rectangle {
    constructor(width, height) {
        this.width = width;
        this.height = height;
    }
    getArea() {
        return this.width * this.height;
    }
}

const rect = new Rectangle(10, 20);
console.log(rect.getArea()); // 200
```

5. **Inheritance**:

```js
class Square extends Rectangle {
    constructor(side) {
        super(side, side);
    }
}

const square = new Square(10);
console.log(square.getArea()); // 100
```

### 5.1.4 JSX

JSX is a syntax extension to JavaScript. It allows you to write HTML-like code in JavaScript.

```js
const element = <h1>Hello, world!</h1>;
```

Needs to be compiled to JavaScript. 


### 5.1.5 React Components

Components are the building blocks of React. They are reusable and can be used to build complex web applications.

The benefits: they are reusable, modular, and easy to maintain. We can also update one component without affecting the others.

**Functional components** are like JavaScript functions. They can take input (props) and return JSX.

```js
const demoComponent = () => {
    return (
        <div>
            <h1>Hello, world!</h1>
        </div>
    );
}
```

**Class components** are like JavaScript classes.

```js
import React, { Component } from 'react';

class DemoComponent extends Component {
    render() {
        return (
            <div>
                <h1>Hello, world!</h1>
            </div>
        );
    }
}

export default DemoComponent;
```

### 5.1.6 Props and State

**Props** are used to pass data from one component to another. They are read-only.

```js
class DemoComponent extends Component {
    render() {
        return <h1>Hello, {this.props.name}</h1>;
    }
}

<DemoComponent name="John" />
<DemoComponent name="Jane" />
```

**State** is the internal data of a component. It is mutable and can be changed.

```js
class DemoComponent extends Component {
    constructor(props) {
        super(props);
        this.state = { name: 'John' };
    }

    render() {
        return (
            <div>
                <h1>Hello, {this.state.name}</h1>
            </div>
        );
    }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<DemoComponent />);
```

### 5.1.7 Passing Data Between Components and Lifecycle Methods

**1. Mounting**: When a component is created, 4 methods are called:
- `constructor()`
- `getDerivedStateFromProps()` (prior to rendering)
- `render()`
- `componentDidMount()` (after rendering)

```js
import React, { Component } from 'react';

class ParentComponent extends Component {
    constructor(props) {
        super(props);
        console.log('1. constructor');
    }

    componentDidMount() {
        console.log('4. componentDidMount');
    }

    render() {
        console.log('3. render');
        return (
            <div>
                <h1>Hello, world!</h1>
            </div>
        );
    }
}
```


**2. Updating**: When a component is updated, 5 methods are called:

- `getDerivedStateFromProps()` (reflect updated props in the state)
- `shouldComponentUpdate()` (access previous props)
- `render()` (update UI per state changes)
- `getSnapshotBeforeUpdate()`
- `componentDidUpdate()` (create side effects)

```js
import React, { Component } from 'react';

class ParentComponent extends Component {
    constructor(props) {
        super(props);
    }
    shouldComponentUpdate(nextProps, nextState) {
        console.log('2. shouldComponentUpdate');
        return true;
    }
    getSnapshotBeforeUpdate(prevProps, prevState) {
        console.log('4. getSnapshotBeforeUpdate');
        return null;
    }
    componentDidUpdate(prevProps, prevState, snapshot) {
        console.log('5. componentDidUpdate');
    }
    render() {
        console.log('3. render');
        return (
            <div>
                <button onClick={() => this.setState({ name: 'Jane' })}>Change Name</button>
            </div>
        );
    }
}
```


**3. Unmounting**: When a component is removed, 1 method is called:

- `componentWillUnmount()` (clean up to prevent memory leaks. e.g. remove event listeners)

**Passing Data from Parent to Child: Props**

**Passing Data from Child to Parent: Callbacks**

Let's review:

```js
import React, { Component } from 'react';
import './ContentRating.css';

class ContentRating extends Component {
   constructor() {
    super();
    this.state = {
      likes: 0,
      dislikes: 0,
      handleLike:() => {
        this.setState((prevState) => ({
          likes: prevState.likes + 1
        }));
      },

      handleDislike:() => {
        this.setState((prevState) => ({
          dislikes: prevState.dislikes + 1
        }));
      }
    }
  }
  render() {
    return (
     <div className='content-rating'>
        <p>---Add text here---</p>
        <div className='rating-buttons'>
        <button className="like-button" onClick={this.state.handleLike}>
            Like ({this.state.likes}) // e.g. Like (5)
        </button>
        <button className="dislike-button" onClick={this.state.handleDislike}>
            Dislike ({this.state.dislikes}) // e.g. Dislike (3)
        </button>
        </div>
    </div>
    );
  }
}

export default ContentRating;
```

## 5.2 Function Components


### 5.2.1 More on Props

Let's do a quick review on props and event handling.

To pass data:

```js
const EmployeeData = (props) => {
    return (
        <div>
            <h1>Employee: {props.name}</h1>
            <p>Department: {props.department}</p>
        </div>
    );
}
```

There can also be default props (immediately before the `export` statement):

```js
EmployeeData.defaultProps = {
    name: 'John Doe',
    department: 'Engineering'
};
export default EmployeeData;
```

In props, define the data using the format `props.attributeName`.


### 5.2.2 Component Composition

To make an "author" component,

```js
import React from 'react';

function Author({ author }) {
    return (
        <div>
            <h1>Author: {author.name}</h1>
        </div>
    );
}

export default Author;
```

To make a "title" component,

```js
import React from 'react';

function Title({ title }) {
    return (
        <div>
            <h2>The {title} is a great book!</h2>
        </div>
    );
}

export default Title;
```

> That's what component composition is! Not a buzzword, right?


**Higher-Order Components (HOCs)**

HOCs are functions that take component(s) and return a new component.

```js
import React from 'react';

function novelBlog({ author, title }) {
    return (
        <div className='novel-post'>
            <Author author={author} />
            <Title title={title} />
        </div>
    );
}

export default novelBlog;
```

The main application will be:

```js
import React from 'react';
import novelBlog from './novelBlog';

function App() {

    const novel = {
        author: 'Haruki Murakami',
        title: 'Norwegian Wood'
    }

    return (
        <div className='app'>
            <novelBlog title={novel.title} author={novel.author} />
        </div>
    );
}

export default App;
```

> That gives a picture of how complex UI is built with components!


### 5.2.3 State Management

**Hooks**: Hooks are functions that allow you to use state and other React features in functional components.

One hook is `useState`. The general format is:

```js
const [stateName, setStateName] = useState(initialState);
```

An example is with colors:

```js
const [color, setColor] = useState('red');
```

> Hey, there is an array here. `color` is the state variable, and `setColor` is the function to update the state.

I will give an example of a button state:

```js
import React, { useState } from 'react';

const [name, setName] = useState('John');

const [buttonClicked, setButtonClicked] = useState(false);

const updateName = () => {
    setName('Jane');
    setButtonClicked(true); // set to true when the button is clicked
}

return (
    <div>
        <p>Name: {name}</p>
        <button onClick={ updateName } disabled={ buttonClicked } >Change Name</button>
    </div>
);
```

Let's do another example of show/hide a component:

```js
import React, { useState } from 'react';

const [isVisible, setIsVisible] = useState(true);

const toggleVisibility = () => {
    setIsVisible(!isVisible);
}

return (
    <div>
        <button onClick={toggleVisibility}>
            {isVisible ? 'Hide' : 'Show'}
        </button>
        {isVisible && <p>This is a paragraph to show/hide.</p>}
    </div>
);
```


### 5.2.4 Functional Components Lifecycle


**1. Mounting**

- Initialization
    - Run function body of the function component
- State initialization
    - Utilize `useState` hook to declare state variables
- Side effects
    - Data fetching, DOM manipulations, etc.
    - Utilizes `useEffect` hook with [] to run only once


**2. Updating**

- Responde to changes of the state


**3. Unmounting**

- Clean up
    - Remove event listeners
    - Cancel network requests
    - Utilizes `useEffect` hook with [] to run only once


**4. Error Handling**

Error boundaries are components that catch errors in their child components and display a fallback UI.


### 5.2.5 Arrays


**Array literal**

```js
const numbers = [1, 2, 3, 4, 5];
const colors = ['red', 'green', 'blue'];
```


**Stateful array**

```js
const [numbers, setNumbers] = useState([1, 2, 3, 4, 5]);
```


**Dynamically constructed array**

```js
const numbers = [];
for (let i = 0; i < 5; i++) {
    numbers.push(i);
}
```

**Traversal methods**

`map()` returns a new array by applying a function to each element of the original array.

```js
const doubledNumbers = numbers.map(number => number * 2);

const numberList = numbers.map(number => <li>{number}</li>);
```


`forEach()` is used to iterate over the array.

```js
numbers.forEach(number => {
    console.log(number);
});
```

`for...of` is also used to iterate over the array.

```js
for (const number of numbers) {
    console.log(number);
}
```

Index access:

```js
for (let i = 0; i < numbers.length; i++) {
    console.log(numbers[i]);
}
```

**Virtual DOM Manipulation**

- React compares the virtual DOM with the previous virtual DOM to determine the changes.
- React then updates the real DOM to reflect the changes.



## 5.3 Hooks and Forms


### 5.3.1 Hooks

Hooks are functions that allow you to use state and other React features in functional components.

Use hooks only in functional components. Call them at the top of the component.

Some common hooks are:

- **useState**: add state to a functional component.

- **useEffect**: perform side effects in functional components.

> **Side effects**: any operation to execute on page onload. They are asynchronous, and may affect the state.

- **useContext**: access the context object.

- **useReducer**: manage complex state logic with a reducer function.

There can also be custom hooks.

```js
function useToggle(initialValue = false) {
    const [value, setValue] = useState(initialValue);
    const toggle = () => {
        setValue(!value)
    }
    return [value, toggle]
}

export default useToggle;
```

```js
function toggleButton() {
    const [isToggled, toggle] = useToggle(false);
    return (
        <button onClick={toggle}>
            {isToggled ? 'ON' : 'OFF'}
        </button>
    );
}

export default toggleButton;
```


### 5.3.2 API Calls

**Application Programming Interface (API)** allows the application to exchange data with external services.

**API fetch methods**: fetch is a built-in function in JavaScript.

```js
fetch('https://api.example.com/data')
    .then(response => response.json()) // parse the response as JSON
    .then(data => console.log(data)) // log the data
    .catch(error => console.error('Error:', error)); // log the error
```


**Axios**: A library for making HTTP requests.

```bash
npm install axios
```

```js
const url = 'https://api.example.com/data';
axios.get(url)
    .then(response => console.log(response.data))
    .catch(error => console.error('Error:', error));
```


### 5.3.3 Forms

**Form handling**

What do we need to handle a form? Input, submission logic, and validation.

React handles forms differently from traditional HTML forms. It uses components, state to store the input, and `setState` to update.

Let's walk through a simple example.

```js
import React, { Component } from 'react';

export default function App() {
    const [email, setEmail] = useState("");
    const handleSubmit = (event) => {
        console.log("Email: , ${ email }");
        event.preventDefault();
    }

    return (
        <form onSubmit={ handleSubmit }>
            <h1>Sign up</h1>
            <label>Email:
                <input type="email" value={ email }
                onChange={ (e) => setEmail(e.target.value) } required />
            </label>
            <button type="submit">Submit</button>
        </form>
    );
}
```

## 5.4 State Management with Redux

### 5.4.1 Redux Basics

**Redux** is a state management library for JavaScript applications. As growing complexity of the application, Redux can manage the state of the application without passing props through multiple components.

**Why Redux?** No need to manage component states. States are managed at the app level. It allows for immutable state properties.

**Redux Elements**:

- **Store**: All current states in the app.
- **Actions**: Object that indicates state change intent.
- **Reducers**: Specifies how to change the state. It receives the current state and action, and returns a new state after performing the action.
- **Dispatch**: Takes an action creator function to return the action and send the object to store.

### 5.4.2 Async

**Synchronous** operations block, but **asynchronous** operations run in parallel.

Javascript **behaves** asynch, but Redux **requires** synch.

**Middleware**: Intercepts actions, delays if necessary, and continues when async completes.
- **Redux Thunk**: Allows for asynchronous actions.
- **Redux Saga**: Allows for more complex asynchronous actions.


### 5.4.3 Redux Toolkit (RTK)

To install RTK, run:

```bash
npm install @reduxjs/toolkit
```

**Slice and store** are the two main components of RTK.

**Slice**: define parts of the application state and logic to update them.

- Application state and logic
- Defined using createSlice()
- Reducer receives current state and action and returns a new state
- Action creators create actions for the store
- Initial state is the initial value

**Store**: combines slices to form application state tree.

- JavaScript object
- Created using the configureStore()
- getState()
- dispatch(action)
- subscribe(listener)


**Integration**:

- `configureStore()`: Slice reducer added to Redux store.

- `combineReducers()`: Combine multiple reducers into a single reducer.

- Actions delegated to appropriate slice reducer.





# 6. Node.js and Express for Back-End

**Node.js** is a run-time environment on the server-side JavaScript applications. **Express** is a server-side JavaScript framework that runs on top of Node.js.


## 6.1 Server-Side JavaScript


### 6.1.1 Basic Concepts

**Types of servers**
- **Database servers**: House, retrieve, and deliver data.
- **Web and HTTP servers**: Serve web pages and handle HTTP requests (give HTTP response).
- **Application servers**: Host and deliver the application through HTTP, sit between a database and a web server.


**Runtime environments**: Like a mini OS, it provides the environment for the application to run.

Why Node.js? It runs on Chrome's V8 engine, which also runs on the front-end browser.

**Back-end responsibilities**: Load (concurrent requests) and Scalability (handle changes in load), Security, Authentication, Walware Detection.


### 6.1.2 Import and Require

**Module specifications** are the conventions and standards to create packages. **CommonJS** and **ES** are two of them.

**CommonJS and Require**:

- `require()` can be called anywhere.
- Dynamic, binding errors identified at run-time.
- Synchronous, blocking.

```js
// message.js
module.exports = "Hello, world!";
```

```js
// main.js
const msg = require('./message.js');
console.log(msg);
```

**ES and Import**:

- `import` can only be called at the top of the file.
- Static, binding errors identified at compile-time.
- Asynchronous, non-blocking.

```js
// message.mjs
const a = 1;
export { a as "myValue" };
```

```js
// main.mjs
import { myValue } from './message.mjs';
console.log(myValue);
```

### 6.1.3 Node.js Modules

Create a simple server using Node.js.

```js
let server = http.createServer((request, response) => {
    let body = "Hello, world!";
    response.writeHead(200, { 
        "Content-Length": body.length,
        "Content-Type": "text/plain"
    });
    response.end(body);
});

server.listen(8080);
```

**package.json**: To specify a different main file, relative path to the Node.js script. NPM (Node Package Manager) requires the name and version.

```json
{
    "name": "mod-today",
    "version": "1.0.0",
    "main": "./lib/today",
    "license": "Apache-2.0",
}
```

**npm**: To install dependencies, run:

```bash
npm install [-g] <package_name>
```

This will create a `node_modules` folder and a `package-lock.json` file. The `-g` flag installs the package globally.



## 6.2 Asynchronous I/O with Callbacks


**Application calls http.request()**:

1. Application calls http.request()
2. Node.js sends the request message to the web server
3. Node.js returns the response message to the application, which does not contain the response body.
4. Node.js receives the response body from the web server.
5. Node.js starts callback to handle web server response.

### 6.2.1 http.request()

```js
http.request(options, function(response) {...})
```

Options need *at least* host ('w1.weather.gov') and path('xml/current_obs/KSFO.xml').

```js
const options = {
    host: 'w1.weather.gov',
    port: 80,
    path: '/xml/current_obs/KSFO.xml',
    method: 'GET',
    headers: {
        'Content-Type': 'application/xml',
        'Content-Length': data.length
    }
}
```

The callback function (optional) is called when the response is received.

**Data** event is emitted when the response body is received.

```js
response.on('data', function(chunk) {
    console.log(chunk.toString());
})
```

**End** event is emitted when the response body is fully received.

```js
response.on('end', function() {
    console.log('No more data');
})
```

**Error** event is emitted when an error occurs.

```js
response.on('error', function(error) {
    console.error(error);
})
response.end();
```

**Two callback functions**: If the main application calls `http.request()`, two callback functions are involved:
- The custom module has a callback function to handle the HTTP response from `http.request()`.
- The main application has a callback function to handle the result captured in the first callback function.


```js
let weather = required('./weather');
let location = 'KSFO';

weather.current = (location, function(temp_f {
    console.log('Temperature at ${location} is ${temp_f} degree F.');
});
```

```js
export.current = (location, resultCallback) {
    ...
    http.request(options, function(response) {
        ...
        response.on('end', function() {
            resultCallback(...);
        });
    }).end();
}
```

### 6.2.2 Promises

**Promises** are objects returned by an asynchronous method. They have three states:
- Pending: initial state.
- Fulfilled: operation completed successfully.
- Rejected: operation failed.

```js
let promise = new Promise(function(resolve, reject) {
    ...
});

promise.then(function(result) {
    ... // fulfilled
}).catch(function(error) {
    ... // rejected
});
```


### 6.2.3 Async/Await

**Async/Await** allows for asynchronous code to be written in a synchronous manner.

```js
async function fetchData() {
    try {
        let response = await fetch('https://api.example.com/data');
        let data = await response.json();
        return data;
    } catch (error) {
        console.error('Error:', error);
    }
}

fetchData();
```

**More Axios**: 

```js
const axios = require('axios');

const data = {
    name: 'John',
    age: 30
}

axios.post('https://api.example.com/data', data)
    .then(response => {
        console.log(response.data);
    })
    .catch(error => {
        console.error('Error:', error);
    });
```

Async/Await handles HTTP requests efficiently. Await pauses function execution for POST requests.




## 6.3 Express


### 6.3.1 Web Frameworks

Node.js is not a framework, but a runtime environment that executes JavaScript code on a server. Node.js requires a web framework to utilize it.

Two approaches to build back-end (not mutually exclusive):
- **Model-View-Controller (MVC)**: Separate the application into three layers: Model, View, and Controller. For apps that need separation of the data, data representation, and manipulation.
    - Koa, Express, Django, NestJS.
- **Representational State Transfer Application Programming Interface (REST API)**: Use HTTP methods to manipulate resources. Allows multiple servers to communicate with each other. Client and server code are independent.


Two purposes of **Express**:
- As an API
- Setup template for Server-Side Rendering (SSR)


### 6.3.2 Start with Express

How to start with Express?
1. Declare Express as a dependency in the package manifest of a Node.js object.
    - Create a `package.json` file.
    - Containing name, version, description, main, and dependencies.
    ```json
    {
        "name": "demo",
        "version": "1.0.0",
        "description": "Retrive current weather from the web server",
        "main": "app.js",
        "dependencies": {
            "express": "4.18.2"
        }
    }
    ```
2. Run the npm command to download missing modules.
    - `npm install`, modules will be downloaded to `node_modules` folder.
3. Import the Express module and create an Express application.
    ```js
    const express = require('express');
    const app = express();
    ```
4. Create a new route handler.
    ```js
    app.get('temperature/:location_code', function(request, response) {
        let location = request.params.location_code;
        weather.current(location, function(error, temp_f) {
            ...
        });
    });
    ```
5. Start an HTTP server on a port.


### 6.3.3 Routing, Middleware, and Templating

**Routing**: handle different routes and requests.

```js
const express = require('express');
const app = express();

let userRouter = express.Router();
let itemRouter = express.Router();

app.use('/users', userRouter);
app.use('/items', itemRouter);

userRouter.get('/about/:id', function(request, response) {
    response.send('User ' + request.params.id);
});

userRouter.get('/details/:id', function(request, response) {
    response.send('User details' + request.params.id);
});

itemRouter.get('/about/:id', function(request, response) {
    response.send('Item ' + request.params.id);
});

itemRouter.get('/details/:id', function(request, response) {
    response.send('Item details' + request.params.id);
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```

```plaintext
localhost:3000/users/about/123
User 123

localhost:3000/items/about/456
Item 456

localhost:3000/items/details/456
Item details 456
```


**Middleware**: functions that have the access to the request object (req), the response object (res), and the next function in the application's request-response cycle.

**1. Application-level middleware** is bounded with `app.use()`.

```js
app.use(function(request, response, next) {
    if (request.query.password !== 'secret123') {
        return response.status(402).send('Unauthorized');
    } else {
        console.log('Time:', Date.now());
        next();
    }
});
```

**2. Route-level middleware** is bounded with `router.use()`.

```js
let userRouter = express.Router();

userRouter.use(function(request, response, next) {
    ...
    next();
});
```

**3. Error-handling middleware** is bounded with `app.use()` or `router.use()`.

```js
app.use(function(error, request, response, next) {
    if (request.params.id === '1') {
        throw new Error('Admin login attempted');
    } else {
        next();
    }
});

app.use(function(error, request, response, next) {
    if (error) {
        response.status(500).send(error.toString());
    } else {
        next();
    }
});
```

**4. Built-in middleware**: for static files, JSON, cookie parser, etc.

```js
app.use(express.static('cad220_staticfiles'));
```

You can also define your own middleware.

```js
function logTime(request, response, next) {
    console.log('Time:', Date.now());
    next();
}

app.use(logTime);
```


**Templating**: Render dynamic content.

```js
const express = require('express');
const app = express();
const expressReactViews = require('express-react-views');

const jsxEngine = expressReactViews.createEngine();

app.set('views engine', 'jsx');
app.set('views', 'myviews');

app.engine('jsx', jsxEngine);

app.get('/:name', function(request, response) {
    response.render('index', { name: request.params.name });
});

app.listen(3000, () => {
    console.log('Server is running on port 3000');
});
```


### 6.3.4 Authentication and Authorization

**Authentication**: Verify user credentials.

**Authorization**: Determine what resources a user has access to.

There are three popular authentication methods:

1. Session-based
    - User logs in with a username and password.
    - Credentials are checked against the database.
    - Session ID created, stored in database and browser cookie.
    - Session ID destroyed on logout or expiration.

```js
const express = require('express');
const session = require('express-session');
const app = express();

// Middleware to set up session management
app.use(session({
  secret: 'secret-key', // Replace with a strong secret key
  resave: false, // Whether to save the session data if there were no modifications
  saveUninitialized: true, // Whether to save new but not modified sessions
  cookie: { secure: false } // Set to true in production with HTTPS
}));

// POST endpoint for handling login
app.post('/login', (req, res) => {
  const { username, password } = req.body;
  // Simulated user authentication (replace with actual logic)
  if (username === 'user' && password === 'password') {
    req.session.user = username;  // Store user information in session
    res.send('Logged in successfully');
  } else {
    res.send('Invalid credentials');
  }
});

// GET endpoint for accessing dashboard
app.get('/dashboard', (req, res) => {
  if (req.session.user) {
    res.send(`Welcome ${req.session.user}`);  // Display welcome
  } else {
    res.send('Please log in first');
  }
});

app.listen(3000, () => console.log('Server running on port 3000'));
```
2. Token-based
    - Token contains: **Header**, **Payload**, **Signature**.
        - Header: type of token and encryption algorithm.
        - Payload: data, e.g. user ID, expiration time.
        - Signature: encrypted hash of the header and payload.
    - Token is stored in the browser cookie (encrypted).
    - Token is sent to the server for authentication.
    - Server verifies the token.

**JWT**: JSON Web Token.

```js
const express = require('express');
const jwt = require('jsonwebtoken');
const bodyParser = require('body-parser');
const app = express();
app.use(bodyParser.json());
const secretKey = 'your-secret-key'; // Replace with a strong secret key

// POST endpoint for user login and JWT generation
app.post('/login', (req, res) => {
  const { username, password } = req.body;
  // Simulated user authentication
  if (username === 'user' && password === 'password') {
    // Generate JWT with username payload
    const token = jwt.sign({ username }, secretKey, { expiresIn: '1h' });
    res.json({ token }); // Send token as JSON response
  } else {
    res.send('Invalid credentials');
  }
});

// GET endpoint to access protected resource (dashboard)
app.get('/dashboard', (req, res) => {
  // Get token from Authorization header
  const token = req.headers['authorization'];
  if (token) {
    // Verify JWT token
    jwt.verify(token, secretKey, (err, decoded) => {
      if (err) {
        res.send('Invalid token');
      } else {
        // Token is valid, send welcome message with username
        res.send(`Welcome ${decoded.username}`);
      }
    });
  } else {
    res.send('Token missing');
  }
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

3. Password-less
    - Biometric authentication, magic link, one-time password, etc.
    - App generates a challenge, encrypted by the public key.
    - Private key decrypts the challenge.
    - User signs the decrypted challenge.
    - App verifies the signature.

```js
const express = require('express');
const bodyParser = require('body-parser');
const nodemailer = require('nodemailer');
const app = express();
app.use(bodyParser.json());
const users = {}; // In-memory storage for demo purposes

// Endpoint to request access and send verification code via email
app.post('/request-access', (req, res) => {
  const { email } = req.body;
  // Generate verification code
  const code = Math.floor(100000 + Math.random() * 900000).toString();
  
  // Store the code in memory (users object)
  users[email] = code;
  // Simulated email sending (for demonstration)
  console.log(`Sending code ${code} to ${email}`);
  res.send('Code sent to your email');
});

// Endpoint to verify the received code
app.post('/verify-code', (req, res) => {
  const { email, code } = req.body;
  // Compare the received code with stored code for the email
  if (users[email] === code) {
    res.send('Access granted');
  } else {
    res.send('Invalid code');
  }
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

Let's take a closer look at the JWT example.

```js
const express = require('express');
const jwt = require('jsonwebtoken');

const JWT_SECRET = 'your-secret-key';

const app = express();

app.use(express.json());

app.post('/login', (req, res) => {
    const { username, password } = req.body;
    
    if (username === 'user' && password === 'password') {
        const token = jwt.sign({ username }, JWT_SECRET, { expiresIn: '1h' });
        res.json({ token });
    } else {
        res.status(401).json({ error: 'Invalid credentials' });
    }
});
```

The app POSTs the token to the server. Then, the server verifies the token. The app should then GET the protected resource.

```js
app.get('/employee', (req, res) => {
    let token = req.headers['Authorization'];
    if (!token) {
        return res.status(401).json({ error: 'No token provided' });
    }

    if (token.startsWith('Bearer ')) {
        tokenValue = token.slice(7, token.length).trimLeft();
    }

    // JWT token starts with 'Bearer '
    jwt.verify(tokenValue, JWT_SECRET, (err, decoded) => {
        if (err) {
            return res.status(401).json({ error: 'Invalid token' });
        }

        const verificationStatus = {
            jwt.verify(tokenValue, JWT_SECRET);
            if (verificationStatus.user === 'user') {
                return res.status(200).json({
                    message: 'Employee details fetched successfully',
                    data: {
                        name: 'John Doe',
                        role: 'Software Engineer'
                    }
                });
        }
    }
});
```

> In reality, you should never hardcode the secret key in the code. We will introduce that in later sections.


### 6.3.5 Best Practices

Although Express does not require a specific structure, it is a good practice to follow some guidelines.

```
/project/
    - /node_modules/: Contain packages, automatically created by npm install.
    - /config/: Database connections, environment variables, API keys.
    - /models/: Data models, specify the type of data stored.
    - /routes/: Routes for all entities, one file for each logical set of routes.
    - /views/: Templates files, which dynamically generate HTML, CSS, JS.
    - /public/: Static files, e.g. images, HTTP, CSS, JS. Should have own subfolder.
    - app.js: Main config for application.
    - routes.js: Central location to access routes. Need to IMPORT all files from /routes and EXPORT them as a single object to app.js.
    - package.json: List of dependencies, scripts, and metadata.
```

**Naming Routes**:

| HTTP method and route | Action |
|------------------------|--------|
| GET /users | Get all users |
| GET /users/:id | Get one user by ID |
| POST /users | Create a new user |
| PUT /users/:id | Update a user by ID |
| DELETE /users/:id | Delete a user by ID |

**HTTP codes**:

| Code | Description |
|------|-------------|
| 200s | OK |
| 300s | Resource has been moved |
| 400s | Client side error |
| 500s | Server side error |


**Test REST APIs**:
- Blackbox test (test as a whole)
- Mocha framework contains a module SuperTest


# 7. Python

> Python is my favorite language. I write Python on a *daily basis* and I'm very proficient in it. Since some programming proficiency is assumed, unfortunately I may skip most concepts.

> However, if you are new to programming, I would recommend the book *Python Crash Course* by Eric Matthes. 

> By the way, for advanced programmers, I recommend *Computer Systems: A Programmer's Perspective* by Randal Bryant and David O'Hallaron. It is a great book to understand how computers work and make one a better programmer (for any programming language).


## 7.1 Basic Pandas

**Data loading**: can be used for csv, json, excel, etc.

```python
import pandas as pd

df = pd.read_csv('data.csv')
```

**Series**: one-dimensional array.

```python
import pandas as pd

s = pd.Series([1, 2, 3, 4, 5])

print(s[3])
print(s.iloc[3])
print(s.loc[1:4])
```

**Series attributes and methods**

- `values`: Returns the Series data as a NumPy array.
- `index`: Returns the index (labels) of the Series.
- `shape`: Returns a tuple representing the dimensions of the Series.
- `size`: Returns the number of elements in the Series.
- `mean()`, `sum()`, `min()`, `max()`: Calculate summary statistics of the data.
- `unique()`, `nunique()`: Get unique values or the number of unique values.
- `sort_values()`, `sort_index()`: Sort the Series by values or index labels.
- `isnull()`, `notnull()`: Check for missing (NaN) or non-missing values.
- `apply()`: Apply a custom function to each element of the Series.

**DataFrame**: two-dimensional array.

```python
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Los Angeles', 'Chicago']
}

df = pd.DataFrame(data)

print(df['Name'])
print(df.iloc[2]) # position
print(df.loc[2]) # label
```

Slicing:

```python
print(df[['Name', 'Age']])
print(df[1:3])
```

Find unique elements:

```python
unique_ages = df['Age'].unique()
```

Conditional filtering:

```python
high_above_102 = df[df['Age'] > 25]
```

Save dataframes:

```python
df.to_csv('trading_data.csv', index=False)
```

**Dataframe attributes and methods**

- `shape`: Returns the dimensions (number of rows and columns) of the DataFrame.
- `info()`: Provides a summary of the DataFrame, including data types and non-null counts.
- `describe()`: Generates summary statistics for numerical columns.
- `head()`, `tail()`: Displays the first or last n rows of the DataFrame.
- `mean()`, `sum()`, `min()`, `max()`: Calculate summary statistics for columns.
- `sort_values()`: Sort the DataFrame by one or more columns.
- `groupby()`: Group data based on specific columns for aggregation.
- `fillna()`, `drop()`, `rename()`: Handle missing values, drop columns, or rename columns.
- `apply()`: Apply a function to each element, row, or column of the DataFrame.


## 7.2 Numpy

**1D Array**:

```python
import numpy as np

a = np.array([1, 2, 3, 4, 5])
```

**2D Array**:

```python
b = np.array([[1, 2, 3], [4, 5, 6]])
```

**Array attributes**:
- `ndim`: Represents the number of dimensions or "rank" of the array.
- `shape`: Returns a tuple indicating the number of rows and columns in the array.
- `size`: Returns the total number of elements in the array.
- `dtype`: Returns the data type of the elements in the array.

```python
print(b.ndim) # 2
print(b.shape) # (2, 3)
print(b.size) # 6
print(b.dtype) # int64
```











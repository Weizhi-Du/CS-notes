# Full Stack Software Engineering

### Author: [Weizhi Du](https://weizhi-du.github.io)

#### *Computer Science and Financial Engineering Student @ WashU*


<br/>

Everyone can be a software engineer, really.

This guide is inspired by and based on the *IBM Full Stack Software Developer* series. Reading this guide is merely a starting point (0 to 1). What makes 1 to N is your dedication on practicing and building your own projects. There should be no prior experience required for Modules 1-4. From Module 5 and onwards, I would recommend the knowledge of at least one programming language, or one introductory course like CSE247. Also, feel free to skip the parts you are already familiar with. Pull out your command line and IDE, and happy coding!

## Content

[1. An Overview of Software Engineering](#1-an-overview-of-software-engineering)

[2. Introduction to Cloud Computing](#2-introduction-to-cloud-computing)

[3. HTML, CSS, and JavaScript](#3-html-css-and-javascript)

[4. Git and GitHub](#4-git-and-github)

[5. React and the Front-End](#5-react-and-the-front-end)


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



# 5.3 Hooks and Forms


## 5.3.1 Hooks

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


## 5.3.2 API Calls

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


## 5.3.3 Forms

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
- **Reducers**: Specifies how to change the state.
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

- `configureStore()`



# index.html 
<div id="root"></div>

# index.js
ReactDOM.render(<p className="header">Hi, my name is slim shady</p>, document.getElementById('root'))
# This is similar to document.createElement (what do I want to create and where do I want to create it )


# Benefits of React as a Library
- It's Composable!
- It's like using lego bricks to build a larger project.
- code is more maintable and more flexible
- it's declarative (tell me what to do and I'll worry about how to get it done)

## imperiative way to create and append child to the root element 

const header = document.createElement('h1')
header.textContent = "Header Goes Here"
header.className('header')
document.getElementById('root').append('h1')


# Building a custom componet

- create a function and return 

function MainContent() {
    return (
        <h1>I'm learning React!</h1>
    )
}

- render funnction  with custom component 

<MainContent />

# JSX

- a flavor of javascript that looks like HTML
- we can write the html that we are used to writing 
- with jSx react is just creating javascript objects 
- jsx is kind of a like a function that when returned returns an objject

const element = <h1 className="header">This is JSX</h1>
console.log(element)

/*
{
    type: "h1", 
    key: null, 
    ref: null, 
    props: {className: "header", children: "This is JSX"}, 
    _owner: null, 
    _store: {}
}
 */

// JSX
ReactDOM.render(element, document.getElementById("root"))

# You can only return a single parent element


const nav = (
    <nav>
        <h1>Website</h1>
             <ul>
                <li>FB</li>
                <li>Twitter</li>
             </ul>
    </nav>
)

ReactDOM.render(nav, document.getElementById('root'))


const page = (
    <div>
        <h1>My awesome website in React</h1>
        <h3>Reasons I love React</h3>
        <ol>
            <li>It's composable</li>
            <li>It's declarative</li>
            <li>It's a hireable skill</li>
            <li>It's actively maintained by skilled people</li>
        </ol>
    </div>
)

# what good is ReactDom

- If you try to just append jsx you'll get objects the job of reactDom is to interpret your code and render real elements that the browser can understand

# Quiz 

1. Why do we need to `import React from "react"` in our files?
React is what defines JSX

2. If I were to console.log(page) in index.js, what would show up?
A JavaScript object. React elements that describe what React should
eventually add to the real DOM for us.

3. What's wrong with this code:
```
const page = (
    <h1>Hello</h1>
    <p>This is my website!</p>
)
```
We need our JSX to be nested under a single parent element

4. What does it mean for something to be "declarative" instead of "imperative"?
Declarative means I can tell the computer WHAT to do 
and expect it to handle the details. Imperative means I need
to tell it HOW to do each step.

5. What does it mean for something to be "composable"?
We have small pieces that we can put together to make something
larger/greater than the individual pieces.


# custom components
- a function is useful because it can do one thing over and over again. That is the same use of a component.


# quiz 

1. What is a React component?
A function that returns React elements. (UI)

2. What's wrong with this code?
```
function MyComponent() {
    return (
        <small>I'm tiny text!</small>
    )
}
```

3. What's wrong with this code?
```
function Header() {
    return (
        <header>
            <nav>
                <img src="./react-logo.png" width="40px" />
            </nav>
        </header>
    )
}

ReactDOM.render(<Header />, document.getElementById("root"))
```


# styling
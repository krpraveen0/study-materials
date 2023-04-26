# Introduction to DOM

# **Objectives**

By the end of this chapter, you should be able to:

- Explain in your own words what the DOM is and how it is created
- Use the document object to manipulate the DOM
- Iterate over DOM elements and add attributes

# **Warning**

Before you continue onto the next section, make sure you have a solid understanding of HTML. We will be using JavaScript to manipulate HTML so if you do not know what HTML `elements` and `attributes` are, this section is going to be challenging. You can work through the first couple sections of [Code Academy HTML + CSS](https://www.codecademy.com/learn/web) to get a better understanding, or check out an excellent tutorial by Shay Howe [here](http://learn.shayhowe.com/html-css/building-your-first-web-page/)

# **What is the DOM?**

From [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model):

> The Document Object Model (DOM) is a programming interface for HTML, XML and SVG documents. It provides a structured representation of the document as a tree. The DOM defines methods that allow access to the tree, so that they can change the document structure, style and content. The DOM provides a representation of the document as a structured group of nodes and objects, possessing letious properties and methods. Nodes can also have event handlers attached to them, and once an event is triggered, the event handlers get executed. Essentially, it connects web pages to scripts or programming languages.
> 

To access the DOM, we make use of the `document` object. This object has properties and functions that we use to access our HTML elements which we can manipulate with JavaScript.

Working with the DOM is one of the more fun parts about using JavaScript because we can add behavior to our web pages. With JavaScript, we can change how a page looks and functions based on events the user makes (clicking, hovering, submitting a form, typing a certain key). As you walk through the next couple sections, think about what you might be able to build with this new knowledge.

# **How to access elements in the DOM**

Let's get started with this sample HTML. Copy and paste this into a file called `index.html` and add an external script tag, or use a `<script></script>` right before the `body` closes. For simplicity, we'll take the latter approach right now.

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    *<!-- make sure for now that your script tag is in the head -->*<title>Document</title>
</head>
<body id= "container">
    <div class="hello">
        Hello World
    </div>
    <div class="hello">
        Hello Everyone!
    </div>
    <a href="#">This link goes nowhere!</a>
    <button>Click me!</button>
    <script>
        *// you can put your JavaScript in here, or include an external file.*</script>
</body>
</html>`

The easiest way to select elements is by their `id` using the `getElementById` function on the `document` object (`document.getElementById`). This returns a **SINGLE** element (because ids must be unique!).

`let container = document.getElementById("container");`

We can also use a function called `querySelector`, which selects a **SINGLE** element using `CSS` selectors. If multiple elements match the query you pass in to `querySelector`, the function will simply return the first matching element that it finds.

`let container = document.querySelector("#container");`

Notice that when we select by id using `querySelector`, we pass in the string `#container`, not `container`. Remember: `querySelector` always expects a CSS selector. In contrast, when we use `getElementById`, we just pass in the string `container` (no hashtag)! Since `getElementById` expects to find an element by id, in this case the hashtag isn't necessary.

To select multiple elements, we can use `getElementsByTagName` or `getElementsByClassName`, or we can use `querySelectorAll` and pass in a `CSS` selector. These will return what appear to be arrays (they are not **exactly** arrays, but for right now, that is not a problem).

`let divs = document.getElementsByTagName("div");
let divs = document.querySelectorAll("div");`

Here is another example using `getElementsByClassName` and the same thing with `querySelectorAll`.

`let divsWithClassOfHello = document.getElementsByClassName("hello");
let divsWithClassOfHello = document.querySelectorAll(".hello");`

As you can see, when you pass in a class name using `getElementsByClassName`, you don't need to start the string with a dot. The function expects to receive a class name - it's in the name of the function! On the other hand, `querySelectorAll` takes in any valid CSS query, which is why you need to pass in `.hello` if you want it to find all elements with a class of "hello."

# **Objectives**

By the end of this chapter, you should be able to:

- Change attributes and values on DOM elements
- Traverse the DOM
- Add, create and remove DOM elements

In this section we'll continue to use the same HTML setup as before. Here we'll use it to examine some functions we can use to traverse the DOM. In case you need it:

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body id= "container">
    <div class="hello">
        Hello World
    </div>
    <div class="hello">
        Hello Everyone!
    </div>
    <a href="#">This link goes nowhere!</a>
    <button>Click me!</button>
    *<!-- make sure for now that your script tag is placed here -->*</body>
</html>`

# **Modifying properties and attributes on elements in the DOM**

We can change the text of an element through the `innerHTML` property.

`let firstDiv = document.getElementsByTagName("div")[0];

firstDiv.innerHTML = "Just changed!";`

This can also be done using the `innerText` property.

`let secondDiv = document.getElementsByTagName("div")[1];

secondDiv.innerText = "Just changed Again!";`

What's the difference between `innerText` and `innerHTML`? You can find it [here](https://stackoverflow.com/questions/19030742/difference-between-innertext-and-innerhtml-in-javascript).

We can also directly manipulate the `CSS` properties for elements (through inline styling) with the `style` property.

`let firstDiv = document.getElementsByTagName("div")[0];

firstDiv.style.color = "red";
firstDiv.style.backgroundColor = "teal";`

Notice that if you're accessing CSS properties using dot notation, you need to camelCase those property names, since `firstDiv.style.background-color` is invalid JavaScript. (Bonus question: what do you think will happen if you try typing this in the console?) However, if you use brackets, you can write the properties the same way as you would in a stylesheet:

`firstDiv.style["background-color"] = "purple"; *// this works too*`

If we want to access/modify attributes on elements, we can do that with `getAttribute` and `setAttribute`:

`let body = document.getElementById("container");

body.getAttribute("id"); *// "container"*
body.setAttribute("id", "new_container");
body.getAttribute("id"); *// "new_container"*`

We can also add and remove classes to elements using `classList`

`let secondDiv = document.getElementsByTagName("div")[1];

secondDiv.classList; *// ["hello"]*
secondDiv.classList.add("another_class");
secondDiv.classList; *// ["hello", "another_class"]*
secondDiv.classList.remove("hello");
secondDiv.classList; *// [another_class"]*`

Notice here that we use methods called `add` and `remove`, not the `push` and `pop` methods we've seen when dealing with arrays. This is because the `classList` isn't actually an array and doesn't have `push` or `pop` methods on it.

# **Nodes vs Elements**

When you read documentation about the DOM, you will see the terms `node` and `element`. In JavaScript these two are different and you can read more about the difference [here](https://stackoverflow.com/questions/9979172/difference-between-node-object-and-element-object). In short, there are many different types of nodes, but the ones we will most often be working with are ELEMENT_NODE and TEXT_NODE (you can see them all [here](https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeType)). Element nodes are HTML elements (`div`, `span` etc.). Text nodes are the actual text of an element node.

# **Traversing the DOM**

Another very common operation when working with the DOM is trying to find elements inside of other elements. When we travel through the DOM in search of something, we are doing what is called DOM `traversal`. Here are a few common methods we can use for finding elements and/or text nodes in relation to an element that we have already found.

`let container = document.getElementById("container");
container.childNodes; *// // this contains all of the nodes (including text nodes) that are children*
container.childNodes.length; *// 11*
container.children; *// this contains all of the elements that are children of the element we have selected*
container.children.length; *// 5*

let link = document.querySelector("a");
link.parentElement; *// <body id="container">...</body>*
link.previousElementSibling; *// <div class="hello">Hello Everyone!</div>*
link.previousSibling; *// text node*
link.nextSibling; *// text node*
link.nextElementSibling; *// <button>Click me!</button>*`

# **Creating elements**

To create elements we use the `.createElement` function on the `document` object and pass in a string with the name of the element that we would like to create. This will just return a new HTML element without any text/attributes or placement on the page!

`let newDiv = document.createElement("div");`

So now that we created this element, how do we place it on the page?

# **Appending elements**

`let button = document.createElement("button");
button.innerText = "I am a button created with JavaScript!";

let container = document.getElementById("container");
container.appendChild(button);`

And now that we created an element, how do we remove one?

# **Removing elements**

`let linkToBeRemoved = document.querySelector("a");

let container = document.getElementById("container");
container.removeChild(linkToBeRemoved);`

# **Changing multiple elements**

So what would happen if we wanted to change all of our divs to have a background color of red? Unfortunately, we can not do that without a loop:

`let divs = document.querySelectorAll("div");
divs.style.backgroundColor = "red"; *// this will not work, try to understand the error you receive!// we have to use a loop for each one instead.***for** (let i = 0; i < divs.length; i++) {
  divs[i].style.backgroundColor = "red"; *// this will work!*
}`

Given the following HTML:

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <div class="header">
    </div>
    <section id="container">
        <ul>
            <li class="first">one</li>
            <li class="second">two</li>
            <li class="third">three</li>
        </ul>
        <ol>
            <li class="first">one</li>
            <li class="second">two</li>
            <li class="third">three</li>
        </ol>
    </section>
    <div class="footer">
    </div>
</body>
</html>`

Write the code necessary to do the following:

1. Select the `section` with an id of `container` without using `querySelector`.
2. Select the `section` with an id of `container` using `querySelector`.
3. Select all of the list items with a class of "second".
4. Select a list item with a class of third, but only the list item inside of the `ol` tag.
5. Give the `section` with an id of `container` the text "Hello!".
6. Add the class `main` to the `div` with a class of `footer`.
7. Remove the class `main` on the `div` with a class of `footer`.
8. Create a new `li` element.
9. Give the `li` the text "four".
10. Append the `li` to the `ul` element.
11. Loop over all of the `li`s inside the `ol` tag and give them a background color of "green".
12. Remove the div with a class of `footer`.

# **Solutions**

You can find solutions to the exercises [here](https://github.com/rithmschool/intermediate_javascript_solutions/blob/master/dom_exercises/script.js)
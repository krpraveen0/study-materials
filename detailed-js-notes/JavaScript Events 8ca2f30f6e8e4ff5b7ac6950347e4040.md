# JavaScript Events

# **Objectives:**

By the end of this chapter, you should be able to:

- Explain what browser events are
- Compare and contrast event capturing and bubbling
- Describe what the event object is and name a few commonly used properties that it includes

Throughout this chapter we'll be using the following HTML as our working example. Feel free to copy and paste this text into your text editor, then open the page in Google Chrome.

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <button class="first_button" onclick="firstClick()">Click me first!</button>
    <button class="second_button" >Click me second!</button>
    <button class="third_button">Click me third!</button>
</body>
</html>`

# **What's an event?**

From [MDN](https://developer.mozilla.org/en-US/docs/Web/Events)

> DOM Events are sent to notify code of interesting things that have taken place. Each event is represented by an object which is based on the Event interface, and may have additional custom fields and/or functions used to get additional information about what happened. Events can represent everything from basic user interactions to automated notifications of things happening in the rendering model.
> 

In a nutshell, events are things we can trigger by interacting with the browser. Here are some potential events we can listen (and then execute some code) for:

- clicking on something
- hovering over something with the mouse
- pressing certain keys
- when the DOM has loaded
- when a form is submitted

You can see a full list [here](https://developer.mozilla.org/en-US/docs/Web/Events).

# **Adding an event listener**

There are three ways that we can add event listeners to our code. Given an element we want to listen to, and a function we want to execute, we can either attach the name of the function to the element in HTML, in JavaScript, or we can use the `addEventListener` method.

Here's some JavaScript code that highlights each one of these approaches:

*`// Option 1: - directly in HTML. Note that in your HTML,// the first button makes reference to a function called firstClick// in the onclick attribute***function** **firstClick**(){
    alert("you clicked the first button!");
}

*// Option 2 - attach the function to the element*
let secondButton = document.querySelector('.second_button');
secondButton.**onclick** = **function**(){
    alert("you clicked the second button!");
}
*// Option 3 - use addEventListener*
let thirdButton = document.querySelector('.third_button');
thirdButton.addEventListener("click", **function**(){
    alert("you clicked the third button!");
});`

So which one is best?

It is often best to either use the second or third option, as these are a bit more customizable, but it is good to know all of your options. In this course, we will primarily be using `addEventListener`.

Let's go back to our initial example, remove the `onclick` attribute from our first button, and add some event listeners to our buttons.

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <button class="first_button">Click me first!</button>
    <button class="second_button" >Click me second!</button>
    <button class="third_button">Click me third!</button>
</body>
</html>`

Just like when changing multiple elements, we need to iterate through each one - we cannot just add an event listener to an array-like object of element nodes.

`let buttons = document.getElementsByTagName("button");

*// this will NOT work - what kind of error do you get?*
buttons.addEventListener("click", **function**(){
    alert("You just clicked a button");
});

*// we have to add the event listener to each button***for**(let i=0; i<buttons.length; i++){
    buttons[i].addEventListener("click", **function**(){
        alert('You just clicked on a button!');
    });
}`

# **Removing an event listener**

Sometimes we want to stop listening for events. To do that we use the `removeEventListener` method, but it has some quirks you should be aware of. Assuming you've still got those alert messages being triggered when you click on a button, let's take a look at the following code:

`let buttons = document.getElementsByTagName("button");

*// this will NOT work*
buttons.removeEventListener("click", **function**(){
    alert("You just clicked a button");
});

*// we have to remove the event listener to each button but this STILL won't work! That is because we are using an annonymous function***for**(let i=0; i<buttons.length; i++){
    buttons[i].removeEventListener("click", **function**(){
        alert('You just clicked on a button!');
    });
}`

In order to successfully remove an event listener, the callback that we pass in can't be an *anonymous* function. Let's clear out all the JavaScript and start from scratch. The code below should work; if you run it, event listeners will be added and then removed, so that nothing happens when you click on a button.

*`// In order to remove, we have to name our function before adding it instead of adding an anonymous function***function** **alertData**(){
    alert("You just clicked a button");
}

**for**(let i=0; i<buttons.length; i++){
    buttons[i].addEventListener("click", alertData);
}

*// since we have named our function, we know which one to remove***for**(let i=0; i<buttons.length; i++){
    buttons[i].removeEventListener("click", alertData);
}`

# **Adding an event to wait for the DOM to load**

Another issue that we may face is when we have code like this:

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script>
        let container = document.getElementById("container");
        container.innerText = "Hello World"; *// This throws an error!*</script>
</head>
<body>
    <div id="container">

    </div>
</body>
</html>`

What's going on here?? Well, since our `script` tag is running before the DOM has loaded, it has no idea what the `<div id="container"></div>` is! What we can do is wait for the DOM to load before executing any JavaScript. This can be done either with the `load` event or the `DOMContentLoaded` event. You can read about the difference between them [here](https://stackoverflow.com/questions/8835413/difference-between-load-vs-domcontentloaded).

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script>
        document.addEventListener("DOMContentLoaded", **function**(){
            let container = document.getElementById("container");
            container.innerText = "Hello World"; *// This works now!*
        });
    </script>
</head>
<body>
    <div id="container">

    </div>
</body>
</html>`

You should get in the habit of always waiting for the DOM content to load before you try to manipulate anything on the page with JavaScript.

# **Objectives**

By the end of this chapter, you should be able to:

- Understand what the `event` object is
- Utilize properties and methods in `event` object
- Refactor code to minimize the amount of event listners

# **Data in the event object**

When an event is triggered, we have access to a special object called the `event` object. Inside of this object we can access quite a few useful values. The event object itself is quite large, but here are two of its most important parts:

- `event.target` - the target element of the event
- `event.preventDefault()` - a function that prevents the default action. This is used commonly to stop a form submission from refreshing the page (which is the default action of a submit event). You don't need to worry too much about this right now.

To see just how large the `event` object is, save this HTML to a file, open it up in Chrome, and take a look in the console after clicking on the container:

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
    <script>
        document.addEventListener("DOMContentLoaded", **function**(){
            let container = document.getElementById("container");
            container.addEventListener("click", **function**(event){
                console.log("Let's look at the event object!", event);
            });
        });
    </script>
</head>
<body>
    <div id="container">
        Click on me!
    </div>
</body>
</html>`

# **Capturing vs Bubbling**

So far we have seen the `addEventListener` function take in two parameters: the name of the event and a callback function. But there is actually a third parameter we can pass in as a boolean called `useCapture` which determines if we use `capturing` or `bubbling`.

From [MDN](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener#parameters)

> Event bubbling and capturing are two ways of propagating events that occur in an element that is nested within another element, when both elements have registered a handle for that event. The event propagation mode determines the order in which elements receive the event.
> 

It's very rare that you'll need to pass in this third parameter (in fact, it's possible you'll get through our entire curriculum without doing it!). But it's good to know that the option is there and what it does.

You can read more about capturing and bubbling [here](http://javascript.info/tutorial/bubbling-and-capturing) and [here](https://stackoverflow.com/questions/4616694/what-is-event-bubbling-and-capturing).

# **Accessing the value of whatever is clicked**

When we listen for events, we sometimes want to know exactly what element triggered the event. We can do this using the `target` property on the `event` object, which is given to us when we use `addEventListener`.

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <ul> Ingredients
        <li>Sugar</li>
        <li>Milk</li>
        <li>Eggs</li>
        <li>Flour</li>
        <li>Baking Soda</li>
    </ul>
</body>
</html>`

Let's access each value using the `event.target` property!

`let listItems = document.querySelectorAll('li');

**for**(let i=0; i<listItems.length; i++){
    listItems[i].addEventListener("click", **function**(event){
        alert("You just clicked on " + event.target.innerText);
    });
}`

# **Adding event listeners to parent elements**

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <ul> Ingredients
        <li>Sugar</li>
        <li>Milk</li>
        <li>Eggs</li>
        <li>Flour</li>
        <li>Baking Soda</li>
    </ul>
</body>
</html>`

In order to alert the text of whatever element we looked for, we can either listen on the parent or listen on each child. Let's examine both options:

*`// OPTION 1: listening on the parent*
let ul = document.querySelector("ul");

*// how many event listeners?*
ul.addEventListener("click", **function**(event){
    alert("You just clicked on " + event.target.innerText);
});

*// OPTION 2: listening on the children*
let listItems = document.getElementsByTagName("li");

*// how many event listeners?***for**(let i=0; i<listItems.length; i++){
    listItems[i].addEventListener("click", **function**(event){
        alert("You just clicked on " + event.target.innerText);
    });
}`

So which one do you think is more efficient? If you guessed the one with fewer listeners, you are right! It's always best to have fewer event listeners, as they consume memory and are difficult to manage when there are many of them.

# **Objectives:**

By the end of this chapter, you should be able to:

- Utilize `localStorage` to save information in the browser
- Compare and contrast `localStorage` and `sessionStorage`
- Add and remove primitives to/from `localStorage`
- Add and remove objects to/from `localStorage`

# **What is localStorage?**

`localStorage` is a mechanism for storing information in the browser for a specific domain. The API is quite easy to use and very minimal - so let's get started with it!

You can read more about it [here](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)

# **localStorage vs sessionStorage**

When you read more about `localStorage` you will also hear about something called `sessionStorage`. [MDN](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) explains them both this way:

> The localStorage property allows you to access a local Storage object. localStorage is similar to sessionStorage. The only difference is that, while data stored in localStorage has no expiration time, data stored in sessionStorage gets cleared when the browsing session ends—that is, when the browser is closed.
> 

What this basically means is:

- `sessionStorage` maintains a separate storage area for each given origin that's available for the duration of the page session (as long as the browser is open, including page reloads and restores)
- `localStorage` does the same thing, but persists even when the browser is closed and reopened.

# **Adding, retrieving and removing from localStorage**

The most important thing to remember is that all of your keys in `localStorage` or `sessionStorage` must be **STRINGS**. `localStorage` stores everything as strings, so it's just good to get in the habit of setting your keys as strings to avoid confusion.

To set something into localStorage we use the `setItem` method and to retrieve we use the `getItem` method (only passing in the key)

`localStorage.setItem("instructor", "Elie");
localStorage.setItem("favoriteNumber", 18);
localStorage.setItem("isHilarious", **true**);

localStorage.getItem("instructor"); *// "Elie"*`

If you refresh the page - you should be able to still retrieve these keys in `localStorage`! Try it out a bit more!

To delete a key we use the `removeItem` function, and to clear everything from `localStorage` for this domain we use `clear`:

`localStorage.removeItem("instructor");
localStorage.clear();`

# **Adding objects**

So far we have only added primitives, which is nice and easy, but what happens when we start adding objects? Well, things get a bit trickier.... Let's see what happens:

`let instructors = ["Elie", "Matt", "Tim"];

localStorage.setItem("instructors", instructors);
localStorage.getItem("instructors");`

When we get the instructors from `localStorage`, we don't have an array anymore - we have a string! Remember, when dealing with `localStorage`, everything gets converted into a string.

In order to get back our original data type, we need to briefly introduce something called JSON. Right now we are going to cover this quickly, but we will be discussing it quite a bit more later on.

From [JSON.org](https://www.json.org/):

> JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write. It is easy for machines to parse and generate.
> 

JavaScript has a built-in JSON object, and on this object are two methods used to convert JavaScript data into JSON, and to parse JSON strings into JavaScript. The JSON object itself can't be called or constructed, and aside from its two methods it has no interesting functionality of its own. You can read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)

- `JSON.stringify` [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/stringify) is used to convert JavaScript to JSON (or stringify)
- `JSON.parse` parses a string as JSON. [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)

Using these two methods allows us to preserve the intended data structure when it is something other than a string:

`let instructors = ["Elie", "Matt", "Tim"];

*// the JSON.stringify call converts the instructors array into a JSON string*
localStorage.setItem("instructors", JSON.stringify(instructors));

*// JSON.parse converts the JSON string back into JavaScript (in this case, a valid array)*
JSON.parse(localStorage.getItem("instructors"));`

Given the following HTML, create a `script.js` file to complete the first two parts.

`<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>DOM Exercise</title>
    <style>
        div {
          width: 50px;
          height: 50px;
          display: inline-block;
        }
        **.brown**{
          background-color: brown;
        }
        **.green**{
          background-color: green;
        }
        **.blue**{
          background-color: blue;
        }
        **.purple**{
          background-color: purple;
        }
        **.yellow**{
          background-color: yellow;
        }
        **.car1** {
         background-color: #8C9C12;
        }
        **.car2** {
         background-color: #1DA788;
        }
        **.car1**, **.car2** {
            margin-left: 0;
        }
    </style>
</head>
<body>
    <h1 id="change_heading">Change Me!</h1>
    SELECTED COLOR <span class="selected">None!</span>
    <section>
        <div class="brown"></div>
        <div class="green"></div>
        <div class="blue"></div>
        <div class="yellow"></div>
    </section>
    <h2>Race!</h2>
    <button>Start the race!</button>
    <br>
    <div class="car1"></div>
    <br>
    <div class="car2"></div>
    <script src="script.js"></script>
</body>
</html>`

# **Part 1**

1. Add the necessary code to wait for the DOM to load to make sure that anything you manipulate in the DOM has loaded. You can do this either using `window.onload` or adding an event listener for `DOMContentLoaded`.
2. Replace the text "Change me" with "Hello World!".
3. When a user hovers over one of the colored boxes change the text to display the color that is being hovered over.
4. Create a new `div` element.
5. Give your new `div` a class of `purple` and style it so that it has a background color of purple.
6. Append your new `div` to the page to the `section` tag.

# **Part 2**

Create a racing game with the two cars. When the race button is pressed, the two cars should move across the screen until one of them is at the end of the screen. When one of the blocks reaches the end - you should alert "winner!"

# **Part 1 + 2 Solutions**

You can find the code [here](https://github.com/rithmschool/intermediate_javascript_solutions/tree/master/events_exercises)

# **Part 3**

For this assignment you will be combining your knowledge of DOM access and events to build a todo app!

As a user, you should be able to:

- Add a new todo (by submitting a form)
- Mark a todo as completed (cross out the text of the todo)
- Remove a todo

# **Part 4:**

Using localStorage, try to store your todos so that if you refresh the page you do not lose what you have added to the list! As a super bonus, try to also save todos that you have marked as complete!

# **Part 3 + 4 Solutions**

You can find the code [here](https://github.com/rithmschool/intermediate_javascript_solutions/tree/master/todo_exercise)
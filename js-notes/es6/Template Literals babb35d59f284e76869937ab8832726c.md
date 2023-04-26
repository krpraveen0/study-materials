# Template Literals

**Template Literals**
Introduced in ES6 is a new way in which we can create a string, and that is the
Template Literal. With it comes new features that allow us more control over
dynamic strings in our programs. Gone will be the days of long string
concatenation!
To create a template literal, instead of ' or " quotes we use the ` character.
This will produce a new string, and we can use it in any way we want.

```jsx
let newString = `A string`
console.log(newString)
```

**Multi-line**
The great thing about Template Literals is that we can now create multi-line
strings! In the past, if we wanted a string to be on multiple lines, we had to use
the \n or new line character.

```jsx
let myMultiString = ' Some text that i want \non two lines!';
console.log(myMultiString)
```

With a Template Literal string, we can just go ahead and add the new line into
the string as we write it.

```jsx
let myMultiString = `Some text that i want 
on two lines!`;
console.log(myMultiString)
```

This will produce a string with a new line in it. The ability to do this with
expressions makes Template Literals a really nice templating language for
building of bits of HTML that we will cover later. But what about
concatenation? Let’s look at how we can dynamically add values into our new
Template Literals.

**Expressions**
In the new Template Literal syntax we have what are called expressions, and
they look like this: ${expression} . Consider the code below

```jsx
let name = `Deepak`;
console.log(`hi my name is ${name}`)
```

The ${} syntax allows us to put an expression in it and it will produce the
value, which in our case above is just a variable that holds a string! There is
something to note here: if you wanted to add in values, like above, you do not
need to use a Template Literal for the name variable. It could just be a regular
string.

```jsx
let name = 'Deepak';
console.log(`hi my name is ${name}`)
```

This will produce the same output. These expressions do more than just let us
put in variables that contain strings in them. We can evaluate any sort of
expressions that we would like.

```jsx
let price = 10;
let tax = 2;

let total = `The total price is ${price*tax}`;
console.log(total)
```

We can also use this with a more complex object.

```jsx
let person = {
    firstName : `Shanti`,
    lastName: `Developer`,
    sayName(){
        return `Hi my name is ${this.firstName} ${this.lastName}`;
    }
};

console.log(person.sayName());
```

Here we have a person object with a sayName() method on it: this uses the
shorthand method definition we looked at in the Objects chapter! We can
access the properties from an object inside of the ${} syntax.

**HTML Templates**
With the ability to have multi-line strings and use Template Expressions to
add content into our string, this makes it really nice to use for HMTL
templates in our code.
Lets imagine that we get some data from an API that looks something like this:

```jsx
let data = {
    "id":1,
    "name":"deepak",
    "base_experience":64,
    "height": 7,
    "is_default": true,
    "order": 1,
    "weight": 78,
};
```

This “imaginary” API is of course the developer With this data structure in
mind, let’s create the markup that would show this developer.

```jsx
function createMarkup(data){
    return `
        <article class='developer'>
            <h3>${data.name}</h3>
            <p>The Developer ${data.name} has base_experience of ${data.base_experience},
            having ${data.order} order with weight of ${data.weight} </p>
        </article>
    `
}

$(document).ready(function(){
    $('#content').html(createMarkup(data));
});
```

Without having to use a library like Handlebars or Mustache we can create
nice and easy-to-use templates in our JavaScript!
Let’s look at our Developer example in action (note: we are using jQuery to
modify the DOM. You can ignore this example if you don’t understand jQuery)

We will have to link the js code in a html page as shown below

developer.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Developer Info</title>
</head>
<body>
    <div id="content"></div>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js" integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4=" crossorigin="anonymous"></script>
    <script src="developer.js"></script>
</body>
</html>
```

developer.js

```jsx
let data = {
    "id":1,
    "name":"deepak",
    "base_experience":64,
    "height": 7,
    "is_default": true,
    "order": 1,
    "weight": 78,
};

function createMarkup(data){
    return `
        <article class='developer'>
            <h3>${data.name}</h3>
            <p>The Developer ${data.name} has base_experience of ${data.base_experience},
            having ${data.order} order with weight of ${data.weight} </p>
        </article>
    `
}

$(document).ready(function(){
    $('#content').html(createMarkup(data));
});
```

The output

![template.PNG](Template%20Literals%20babb35d59f284e76869937ab8832726c/template.png)

**Tagged Templates**
Another features of Template Literals is the ability to create Tagged Template
Literals. The way this works is that you create a function and this function
will look like any other function, however when you execute it, that is when it
looks different. Consider the function below.

```jsx
function myTaggedLiteral(strings,value,value2){
    console.log(strings,value, value2);
}

let someText = 'clean';
myTaggedLiteral`test ${someText}`
```

First off, you will notice there are no () when we call the function! We apply
a Template Literal where the parentheses would be. As a parameter to our
function we get an array of the strings in our literal. Let’s expand on the string
we send to the function and we will have it include an expression, and we will
include a new parameter in our function as well.

```jsx
function myTaggedLiteral(strings,value,value2){
    console.log(strings,value, value2);
}

let someText = 'clean';
myTaggedLiteral`test ${someText} ${2+3}`
```

When we use an expression we can access that from the next parameters and
this keeps going. Say we added another expression.

```jsx

```

This is pretty powerful: it allows you to take the data used in a string and
manipulate it to your liking.

**Reusable Templates**
Let’s look at a simple use case for this. If you remember from above, we saw
how Template Literals work really great for, well, making templates! Let’s take
that a step further and create a function that would allow us to create
reusable templates. The idea here is that we can create the initial template
and then pass in data for it to use later.

```jsx
const student = {
    name: 'deepak',
    blogUrl: 'engineeringcoders.com'
}

```

Let’s look at implementing our templater function

```jsx
const studentTemplate = templater `
    <article>
        <h3>${'name'} is a student at EgnineeringCoder</h3>
        <p> You can find there work at ${'name'} .</p>
    </article>
`;

const myTemplate = studentTemplate(student)
console.log(myTemplate);
```

The first thing you will notice is this ...keys parameter. The ... syntax is
what’s called Rest Parameters; it basically will gather any parameters the
function has and create an array for us. We will dig deeper into that in the
Spread Operator & Rest Parameters chapter.
The next thing we want to do is return a function that is going to access our
object. The returning of the function is what allows us to call and pass in our
student data, like this: studentTemplate(student) .

```jsx
const templater = function(strings,...keys){
    return function(data){
    }
};
```

With this data now available to us we need to perform some manipulation.
The process is as follows. First, we need to create a copy of the strings array.
We make a copy in case we want to reference the original later. Then we need
to loop through the array of keys , and for each one of those, grab the data
from the object that matches the key (notice how in this example we pass in a
string in the ${} ) and place it in our array where needed. Finally, we need to
join it all back together as a string and return it from the function!

```jsx
const templater = function(strings,...keys){
    return function(data){
        let temp = strings.slice();
        keys.forEach((key,i)=>{
            temp[i] = temp[i] + data[key]
        });
        return temp.join(' ');
    }
};
```

Let’s see our example in action:

```jsx
const student = {
    name: 'deepak',
    blogUrl: 'engineeringcoders.com'
}

const templater = function(strings,...keys){
    return function(data){
        let temp = strings.slice();
        keys.forEach((key,i)=>{
            temp[i] = temp[i] + data[key]
        });
        return temp.join(' ');
    }
};

const studentTemplate = templater `
    <article>
        <h3>${'name'} is a student at EgnineeringCoder</h3>
        <p> You can find there work at ${'name'} .</p>
    </article>
`;

const myTemplate = studentTemplate(student)
console.log(myTemplate);
//ouput
```

ouput:

```python
<article>
        <h3>deepak  is a student at EgnineeringCoder</h3>
        <p> You can find there work at deepak  .</p>
    </article>

```

You will notice that this is not an exhaustive example. We have no way to
accommodate nested data or array values; it is simply just strings. But I hope
this example helps to illustrate what you can start doing with Tagged
Template Literals.
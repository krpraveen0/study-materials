# Debugging

# **Objectives:**

By the end of this chapter, you should be able to:

- List common errors in JavaScript and how they are created
- Understand the difference between a TypeError and ReferenceError
- Use try/catch statements to handle errors gracefully and throw errors when necessary

# **What is An Error**

An error is a problem in your code that may or may not stop the code from running. An error in a JavaScript program occurs for one of two main reasons: either the code that is written is not valid JavaScript code, or the code is valid, but it is trying to do something that is not allowed. In the next sections we will talk about some common examples.

# **How Errors work in JavaScript**

All errors in JavaScript are actually `objects` that are created by a function called `Error`. You can read more about it [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Error). As MDN says, "error objects are thrown when runtime errors occur. The Error object can also be used as a base object for user-defined exceptions."

So what does this mean? A runtime error is an error that occurs when code is executed. For example, if you hop into the Chrome console and write some invalid JavaScript (e.g. `let 8 = 9;`), you won't actually see any errors show up until you try to run the code.

JavaScript has many built-in errors, which we'll talk about in just a moment. But you can also create and throw your own errors in applications that you write (this is what is meant by a "user-defined exception").

# **Common JavaScript Errors**

Let's look at four common errors we encounter when writing JavaScript. You have probably seen quite a few of these before!

- `SyntaxError` - occurs when we make a mistake with our syntax:

`let x = "hello";

let wrongObj = {
    name: "foo"
    missingComma: **true**
};`

- `ReferenceError` - occurs when we try to access a variable that does not exist in that scope. In the example below, we will try to access a variable called `amazing` which has not yet been initialized. We will then try to access a variable called `secret` outside of its scope. Let's see what that looks like:

`amazing; *// ReferenceError - does not exist in the global scope***function** **defineSomething**(){
    let secret = "I'll never tell";
}

defineSomething();

secret; *// ReferenceError - only exists in the scope of the defineSomething function*`

- `TypeError` - occurs when you make incorrect use of certain types in javascript. That could mean trying to invoke something that is not a function, or accessing properties on undefined. Here are some very common examples (many of them we guarantee you will make!)

**`undefined**(); *// TypeError - undefined is NOT a function!*

let obj = {
    name: "Elie"
};

obj.something; *// this actually returns undefined! What does that tell us? If you try to access a property on an object and it does not exist, you do NOT get a ReferenceError, you just get undefined*

obj.something.foo; *// but when you try to access a property on `undefined`... well, that's a TypeError.*

obj.something(); this is a TypeError **for** the same reason that **undefined**() is, since obj.something is **undefined**!`

- `RangeError` - occurs when we have a function that calls itself (also known as a recursive function). If we have too many functions that have been called (before they are returned) we run out of memory and cause a RangeError.

**`function** **callMe**(){
    callMe();
}

callMe(); *// maximum call stack size exceeded. We will talk more about the call stack and recursion in a later section.*`

Recursion is a more advanced concept that we won't touch on much in this course. It's good to know about this error, but if you're not writing recursive functions it's much less likely that you'll encounter it.

# **Catching and Throwing Errors in JavaScript**

When an error is thrown, our code stops executing. Sometimes we don't know if our code is going to throw an error or not, so instead of our code crashing and not continuing to run, we might want to gracefully handle our errors. We call this "catching" our errors. To do this we use a `try / catch` statement. We place code inside of the `try` block (a block is defined as code inside of a `{}`) and if an error is thrown, the code moves to the `catch` block. After the catch block, code continues to execute.

**`try** {
    thisDoesNotExist;
} **catch**(e) {
    console.log("The error is ", e);
}`

On the other hand, when developing applications or libraries, we sometimes want to throw an error when something is done incorrectly in our application. To return an error and stop code execution, we use the `throw` keyword followed by an error object. Optionally, we can add a message string to the error to give more details about what went wrong.

**`throw** ReferenceError("That variable does not exist!");`

Another way to specify an error is to use the `throw` keyword followed by a string:

**`throw** "This will also be an error";`

Let's write a small example to see what it would be like using `throw`, `try`, and `catch`. In this example, all we are doing is generating a random number between 0 and 1. If that number is >= 0.5, we create an error and so we move to the `catch`. However, our code continues to run even if an error happens.

**`try** {
    **if**(Math.random() >= .5) {
        **throw** "Let's make an error!";
    }
    console.log("Whew...we made it.");
    console.log("We can only get here if the random number is less than .5.");
} **catch**(e){
    console.log("The error is ", e);
    console.log("We can only get here if an error was thrown. (Random number is greater than .5).");
}

console.log("Moving on.....");`

# **`finally`**

With our `try/catch` block, we saw that the code in the `try` block will move to the catch block if an error occurs inside of it. In our `try/catch` statements, we can add one more special keyword called `finally`. Inside of the `finally` block, code will execute regardless of an error being thrown.

**`try** {
    *// let's randomly try to throw an error***if**(Math.random() >= .5){
        *// The following code will throw:// Uncaught TypeError: undefined is not a function(…)***undefined**();
    }
    console.log("Whew, we made it");
} **catch**(e){
   console.log("We didn't make it. The error message is", e.message);
} **finally** {
   console.log("No matter what we will see this statement");
}`

# **Objectives**

By the end of this chapter, you should be able to:

- Use the sources tab to create snippets
- Use the sources tab to set breakpoints to stop code execution
- Utilize the `debugger` keyword to write better code faster

# **Introduction to The Sources Tab**

The developer tools in chrome are very powerful and useful tools that will help tremendously as you start to understand issues in your code. As a reminder, you can open up the developer tools by holding `command` + `option` + `j` on a mac or `control` + `shift` + `j` on a windows machine.

In this lesson, we will be talking mainly about the sources tab. After you open the developer tools, you can click on the appropriate tab labeled `Sources`. The tab allows you, the developer, to see the javascript code that is being run on your website. With the developer tools, you have the ability to stop the code at a certain point to see exactly what values variables are holding as the code is being run.

To demonstrate how to debug JavaScript code in the sources tab, we will use another feature of the developer tools called code snippets. Using code snippets, you can write and save pieces of javascript code which you can then run and debug. The following video will show you how to get to the sources tab, create a snippet, and create break points in the code to see what values different variables have as the code is being run.

# **Getting Started with the sources tab**

Watch a quick walkthrough of the sources tab and check out the content below for some supplemental material:

# **Additional Sources Tab Features**

If you would like to read more about the sources tab and some other useful tools you can find them at [https://developers.google.com/web/tools/chrome-devtools/debug/breakpoints/step-code?hl=en](https://developers.google.com/web/tools/chrome-devtools/debug/breakpoints/step-code?hl=en)

CodeSchool also offers a free course on the Chrome Dev Tools which you can find at [http://discover-devtools.codeschool.com/](http://discover-devtools.codeschool.com/)

Answer the following questions:

- What does the `throw` keyword do?
- What does the `finally` keyword do?
- What is the difference between a `TypeError` and `ReferenceError`?
- How do you create a snippet in the Chrome dev tools?
- In the Chrome dev tools, on the right hand side of the sources tab, there is a "pause" button which allows you to "pause on caught exceptions." What is an `exception`?
- How do we "catch" errors in JavaScript? Give an example with code for what that might look like.

Explain what type of error will be thrown, why the error is occuring, and how to fix it:

1.

`person;`

2.

`let data = {};
data.displayInfo();`

3.

`let data = {};
data.displayInfo.foo = "bar";`

4.

**`function** **data**(){
    let thing = "foo";
}
data();
thing;`

# **Part II**

Fix the broken code and explain what was wrong:

1.

**`for**(let i=0; i > 5; i++){
    console.log(i);
}`

2.

**`function** **addIfEven**(num){
    **if**(num % 2 = 0){
        **return** num + 5;
    }
    **return** num;
}`

3.

**`function** **loopToFive**(){
    **for**(let i=0, i < 5, i++){
        console.log(i);
    }
}`

4.

**`function** **displayEvenNumbers**(){
    let numbers = [1,2,3,4,5,6,7,8];
    let evenNumbers = [];
    **for**(let i=0; i<numbers.length-1; i++;){
        **if**(numbers % 2 = 0); {
            evenNumbers.push(i);
        }
        **return** evenNumbers;
    }
}
displayEvenNumbers(); *// should return [2,4,6,8]// HINT - eight things need to be changed here for this to work!// Start by fixing the syntax errors and then run the function to see what your output is.*`

# **Solutions**

You can find solutions to the exercises [here](https://github.com/rithmschool/intermediate_javascript_solutions/tree/master/debugging_exercise)
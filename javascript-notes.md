# JavaScript

What is JavaScript ?

JavaScript (JS) is a lightweight, interpreted, or just-in-time compiled programming language with **first-class functions.**

Where **just-in-time** **compilation** or **run-time compilation** is a way of executing computer code that involves compilation during execution of a program (at run time) rather than before execution.

**first-class function:** A programming language is said to have **First-class functions** when functions in that language are treated like any other variable.

```jsx
const item = function() {
   console.log("items");
}
// Invoke it using the variable
item();
```

Note: In above example: Anonymous Function in a Variable (item) , then we used that variable to invoke the function by adding parentheses **()** at the end.

Note: Even if the function is named then variable name can be used to invoke it, Naming the function helps in debugging the code.

**Passing function as an argument :**

```jsx
function argumentFunc() {
   return "I am a function passing as an argument to other function";
}
function secondFunc(argFunc, name) {
  console.log(argFunc() + name);
}

greeting(argumentFunc, "JavaScript!");
```

In the above code We are passing our argumentFunc() function as an argument to the secondFunc() function, this explains how we are treating the function as a value.

Note: The function that we pass as an argument to another function, is called a **Callback function**. In above program **argumentFunc** is a Callback function.

**Function returning a Function:**

```jsx
function Person() {
   return function() {
      console.log("Student!");
   }
}
```

**Note: A function that returns a function is called a Higher-Order Function**

In above example Person is a Higher-Order Function

Now to invoke the function inside a function 

1. by using variable
2. by using double parenthesis.

1. by using variable:

```jsx
const outerFunc = function() {
   return function() {
      console.log("Inner FUnction!");
   }
}
const myFunc = outerFunc();
myFunc();
```

Note: In above program We have used another variable myFunc. If we invoked outerFunc directly(without any parenthesis), it would return the function itself without invoking its returned function.

1. by using double parenthesis:

```jsx
 const outerFunc = function() {
   return function() {
      console.log("Inner FUnction!");
   }
}
outerFunc()();
```

Note: In above program we are using double parenthesis to invoke the inner returned function as well.

[Course Content ](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Course%20Content%201ccb686be1ad4e6089a16766267b8f04.md)

[Introduction to JS](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Introduction%20to%20JS%20cde7f39eb1104da8b402de21d5c97826.md)

[How JS works or executed in JS Engine](JavaScript%20c580c2030d7f48599e1750745bffcc9f/How%20JS%20works%20or%20executed%20in%20JS%20Engine%205bf7c6221fc8421997572b9627742034.md)

[Comments](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Comments%20bc2f984c6ac449acbf0b00bd0cb7c770.md)

[Data types in JS](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Data%20types%20in%20JS%207fa69fcafe8048d0a290a08d54a97d79.md)

[null, Undefined and Symbol](JavaScript%20c580c2030d7f48599e1750745bffcc9f/null,%20Undefined%20and%20Symbol%20b76b7ba7cf614a8c947421dec9af4533.md)

[object type in JS](JavaScript%20c580c2030d7f48599e1750745bffcc9f/object%20type%20in%20JS%207f83197d77c84f0faf5eab8c126f90ab.md)

[Introduction Arrays](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Introduction%20Arrays%20e5d39c9609f942f7a2e206fcead6ba99.md)

[Functions](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Functions%2036e75c915e794582b223d11d73215a3b.md)

[typeof operator](JavaScript%20c580c2030d7f48599e1750745bffcc9f/typeof%20operator%2011a0682a48284e27810ca462382aa31a.md)

[Some more operators](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Some%20more%20operators%20b0a98d023dae4f508a7ae92d845e53f0.md)

[Conditional Statements](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Conditional%20Statements%20096d99a47a1d474c8483112067ef1946.md)

[switch statement](JavaScript%20c580c2030d7f48599e1750745bffcc9f/switch%20statement%2096bf443a11e3467fae7211bee6ffa9b9.md)

[Iterative statements](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Iterative%20statements%209b75ca9abe8641528529eb5dcc073f6c.md)

[Value and Reference Types](JavaScript%20c580c2030d7f48599e1750745bffcc9f/Value%20and%20Reference%20Types%200eb5d6fe71f94d4bb7fcee09ec392a29.md)

[ES6](JavaScript%20c580c2030d7f48599e1750745bffcc9f/ES6%20f642ff75858e47b6aa3542696e944cd3.md)
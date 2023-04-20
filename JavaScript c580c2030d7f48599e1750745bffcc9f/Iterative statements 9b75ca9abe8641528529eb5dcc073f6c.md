# Iterative statements

**Iteration Statements**

Let’s see iteration. In order to execute the same expressions multiple times, we create loops.

Example: repeating same line of in a song again & again.

**While Loop**

Learn how to repeat your code as many times as you want, by just writing down your code once.****

Let’s create a function that sums the values of an array:

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

Program to add marks of all student’s in a class

```jsx
let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

let i = 0;

while ( i < values.length ) {

sum += values[i];

i += 1;

}

console.log( 'The loop was executed ' + i + ' times' );

return sum;

}

sumArray( numbers );
```

In above program

First the JavaScript interpreter examines the condition in the while loop. As i is 0 and numbers.length is 13 , we conclude the condition is true.

If the condition is true, we execute the body of the while loop. So we add the ith element of the array to the sum, and increase the loop variable by 1 .

Then we compare 1 against the length of the array, 13 . As 1 is smaller than 13 , we execute the loop body again. The sum variable now stores 19 + 65 = 84 . The value of i becomes 2 .

We continue this until i becomes 13 . Then we realize the condition i < numbers.length becomes false . Once the condition of the while loop becomes false , we continue with the code after the while loop.

**Do-While Loop**

The do-while loop executes the loop body at least once, and checks the condition before the end.

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

if ( values.length == 0 ) return 0;

let sum = 0;

let i = 0;

do {

sum += values[i];

i += 1;

} while ( i < values.length );

console.log( 'The loop was executed ' + i + ' times' );

return sum;

}

sumArray( numbers );

We mainly use do-while loops for input validation. The user inputs a value, then we check its validity.

Let’s use the prompt function to get a value. prompt( ‘message’ ) opens a dialog displaying message.

A text field appears in the dialog, where we can enter a value. Once we press the OK button, the prompt function returns a string.

This is where the do-while loop makes sense, because we can be sure we need to enter data at least once. In the example summing array members, using the do-while loop is technically possible, but it does not make sense, because the simple while loop is easier

**For Loop**

We will now learn another loop that is perfect for iteration: the for loop. This loop combines several lines of code into one. The execution of the for loop is identical to the while loop:

Below is the syntax of while loop and for loop

initialization_of_loop_variable;

while ( condition ) {

statements;

Increment_loop_variable;}

for ( initialization_of_loop_variable; condition; increment_loop_variable ) {

statements;

}

The for loop has everything we need in one line.

We don’t have to mix our loop body with the increment of the loop variable.

The execution of the for loop is as follows:

1. initialization_of_loop_variable

2. check the condition . If condition is falsy, exit the for loop

3. statements in the loop body

4. increment_loop_variable , then go back to step 2

Lets rewrite the sum of students marks function using a for loop. Here is the example with the while loop:

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

let i = 0;

while ( i < values.length ) {

l [i]

sum += values[i];

i += 1;

}

return sum;

}

sumArray( numbers );

Using for loops:

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i = 0; i < values.length; i += 1 ) {

sum += values[i];

}

}

sumArray( numbers );

Notice in the above program we have declared variables in the initializer part of the for loop.

The rest of the code works exactly like the while loop.

Let’s simplify the for loop a bit further: you can write i++ or ++i in place of i += 1 :

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i = 0; i < values.length; ++i ) {

sum += values[i];

}

}

sumArray( numbers );

**Some optimization techniques**

In some programming competitions, people tend to count downwards instead of upwards. The reason is that computing values.length costs some nanoseconds more than checking if the value of i is positive:

for ( let i = values.length - 1; i >= 0; --i ) {

sum += values[i];

}

These wannabe geniuses don’t stop there by the way. They go even further

In above code Instead of iterating from 12 to 0 , we iterate from 13 to 1 . The condition i is true as long as its value stays non-zero. This is the easiest check a computer can make with an integer.

Suppose i is 13 . values[–i] is interpreted as values[12] , because first we decrease the value of i , then we equate the expression –i to the new value of i .

This is a unique case when writing i– would have been incorrect, because our array does not even have an element at index 13 .

The above code save some nano seconds but it decreases the readability of the code.

Another reason to avoid looking smart and optimizing your code is that JavaScript interpreters actually optimize code for us. This is a very easy and straightforward optimization. We don’t have to bother doing it ourselves.

We Just need to stick to this version of the for loop ie

for ( let i = 0; i < values.length; ++i ) {

sum += values[i];

}

**Some more Loops**

1. for…in loop :

> The for…in loop enumerates all the available indices of the values array from 0 to 12 in ascending order.
> 
> 
> Example:
> 

for ( let i in values ) {

sum += values[i];

}

> The above form of for loop avoid writing the iterating variable code ie
> 
> 
> Why bother iterating an i variable if a loop can take care of it for us?
> 
1. for…of loop

> for…of loop enumerate the values of the array which answers
> 
> 
> “why bother using a variable for iteration at all?”
> 
> It was introduced in ES6 .
> 

for ( let value of values ) {

sum += value;

}

> Break and Continue
> 
> 
> We can use break or continue inside the loops:
> 
> break exits the closest loop it is in, and continues with the next command, continue skips out from the loop body, and jumps back to the condition of the loop.
> 
> Continue
> 
> sum every second element of the numbers array
> 

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i in values ) {

if ( i % 2 == 0 ) continue;

sum += values[i];

}

return sum;

}

console.log("The sum is", sumArray( numbers ));

> we are testing continue just for the sake of the example. Whenever i is even, continue moves execution back to the next iteration of i in values .
> 
> 
> As above in code we can Notice that we don’t have to use braces around just one statement in the code if it is followed by an if statement or a loop:
> 

> The above code is same as
> 

if ( i % 2 == 0 ) {

continue;

}

> Break
> 
> 
> When break is executed, control is handed over to the statement after the loop.
> 
> We already know what a break statement looks like, because we learned it when dealing with the switch statement.
> 
> It is doing the same thing in loops.
> 
> Suppose we want to break out from the loop whenever the sum exceeds 100:
> 

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i in values ) {

sum += values[i];

if ( sum >= 100 ) {

break;

}

}

return sum;

}

sumArray( numbers );

> We placed the break in braces on purpose to show you that break breaks out of switch statements and loops, not from if statements.
> 
> 
> When break is executed, control is handed over to the statement after the loop: return sum .
> 
> In this specific example, we don’t even need a break , because instead of breaking out of the loop, we can return the sum
> 

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i in values ) {

sum += values[i];

if ( sum >= 100 ) return sum;

}

return sum;

}

sumArray( numbers );

> Technically, this is an example, where we can write more flexible for loop:
> 

let numbers = [19, 65, 9, 17, 4, 1, 2, 6, 1, 9, 9, 2, 1];

function sumArray( values ) {

let sum = 0;

for ( let i = 0; i < values.length && sum <= 100; ++i ) {

sum += values[i];

}

return sum;

}

sumArray( numbers );

> Task:
Create a random number using the expression below
> 
> 
> Math.trunc( Math.random() * 10 ) + 1
> 
> The above expression creates a random number between 1 and 10.
> 
> Create a function that asks the user for a number between 1 and 10 and repeat the question until a correct number is entered.
> 
> Help: prompt( ‘Message’ ) gives you a popup displaying ‘Message’ and asks for an input.
> 
> The return value of the prompt function is the input (string).
> 
> The solution
> 

let value = Math.trunc( Math.random() * 10 ) + 1

function guessValue( value ) {

let guess;

do {

guess = prompt( 'Enter your guess (1 - 10):' );

} while ( guess != value );

}

guessValue(value); //calling the function

> Let’s add some more functionality
> 
> 
> Your program should now also print one of the following messages once a value is entered:
> 
> “The value you entered is too high! Try entering a lower number!”
> 
> “The value you entered is too low! Try entering a higher number!”
> 
> “Correct! 36 is the right answer.” - here, assume 36 was the number you had to guess
> 
> “Invalid guess! You have to enter a number between 1 and 50.”
> 
> “Invalid format! Only numbers are allowed!”
> 
> Hint: You can use the alert function to print messages. The alert(“message here”) method displays a pop-up box with a specified message and an OK button.
> 
> Solution:
> 

function logHintOnGuess( guess, value ) {

guess = Number.parseInt( guess, 10 );

if ( Number.isNaN( guess ) ) {

alert( "Invalid format! Only numbers are allowed!" );

} else if ( guess < 1 || guess > 10) {

alert( "Invalid guess! You have to enter a number between 1 and 1

0." );

} else if ( guess > value ) {

alert( "The value you entered is too high! Try entering a lower number!" );

} else if ( guess < value ) {

alert( "The value you entered is too low! Try entering a higher nu

mber!" );

} else if ( guess == value ) {

alert( "Correct! " + value + " is the right answer." );

}

}

let value = Math.trunc( Math.random() * 10 ) + 1

function guessValue( value ) {

let guess;

do {

guess = prompt( 'Enter your guess (1 - 10):');

logHintOnGuess( guess, value ); //calling the Hint function here

} while ( guess != value );

}

guessValue(value); //calling the function

> Value and Reference Types
> 
> 
> JavaScript does not give us full access to our data structures in memory. However, reference types still exist in the language. Mixing value and reference types comes with unwanted side-effects and bugs.
> 
> Understanding the difference between value and reference types plays a vital role in writing robust programs.
> 
> Note:
> 
> Numbers, booleans, strings, null and undefined are primitive types.
> 
> All primitive types are passed by value.
> 
> Objects, arrays, and functions are passed by reference.
> 
> Strings are somewhat special in JavaScript.
> 
> Unlike many other languages, strings are not defined as arrays of characters. What is more, the character type does not even exist in JavaScript.
> 
> Strings are immutable data types, with an interface that makes them look like an array of characters.
> 
> In practice, any modifications to a string result in a new, immutable string value.
> 
> After the introduction of value and reference types, let’s continue with a riddle. Determine the result of the console logs.
> 

var people = [

{ name: 'John Hill', age: 22 },

{ name: 'Jack Chill', age: 27 }

];

var getInitials = function( name ) {

// Reusing the name argument makes little sense in general.

// We are making this assignment here for demonstrating

// the difference between value types and reference types.

name = name.split( ' ' ).map( function( word ) {

return word.charAt( 0 );

} ).join( '' );

console.log( name );

return name;

}

var increaseAge = function( person ) {

person.age += 1;

}

var addPerson = function( people, name, age ) {

people.push( { name: name, age: age } );

}

// Part 1: getInitials

console.log( getInitials( people[0].name ) );

console.log( people[0].name );

// Part 2: increaseAge

increaseAge( people[1] );

console.log( people[1].age );

// Part 3: addPerson

addPerson( people, 'Jim Gordon', 32 );

console.log( people );
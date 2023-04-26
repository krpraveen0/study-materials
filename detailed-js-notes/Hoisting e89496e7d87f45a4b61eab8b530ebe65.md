# Hoisting

# **Objectives**

By the end of this chapter, you should be able to:

- Explain where a variable name gets defined in your code
- Describe how hoisting affects function expressions vs function declarations
- Write functions that call other functions
- Understand what function decomposition is and how to break up your functions

# **Hoisting**

From [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#let_hoisting):

> Because variable declarations (and declarations in general) are processed before any code is executed, declaring a variable anywhere in the code is equivalent to declaring it at the top. When we used to use the var keyword, it meant that a variable could appear to be used before it's declared. This behavior is called "hoisting", as it appears that the variable declaration is moved to the top of the function or global code. When we use the let and const keyword, we simply can not access a variable before it is declared. You will encounter hoisting when you compare function declarations and function expressions.
> 

# **Hoisting In Function Declarations vs Function Expressions**

So how does this work with function declarations vs function expressions?

Function declarations are fully defined before the code is run. So in the following example, we can call the `sayHi` function above the lines that define the `sayHi` function:

`sayHi("Matt"); *// "Hello Matt"***function** **sayHi**(name){
    **return** "Hello " + name;
}`

However, function expressions act differently. In the following example, there is an error because we are trying to invoke a function called `sayHi` but at that point in the code `sayHi` is not equal to a function. In fact, `sayHi` exists in memory but we can not access it and JavaScript will throw an error.

`sayHi("Matt"); *// Throws an error!*

let **sayHi** = **function**(name){
    **return** "Hello " + name;
}`

This is why we recommend that for now, you just use function declarations where you do not need to use the `let` or `const` keyword.

You can read more about hoisting [here](https://developer.mozilla.org/en-US/docs/Glossary/Hoisting).

# **Functions with a single responsibility**

Now that you've gotten some more experience writing functions, let's examine a best practice when writing functions. When writing functions, you should strive to make your functions do one thing and do them well. Instead of trying to combine different pieces of logic all into one function, write smaller functions that each do one thing well independently, and then call your functions in other functions. Let's see what we mean!

### **Calling functions from other functions**

Let's imagine we need to write a function that accepts an array of values and returns the lowest number in the array and console.log's any values that are not a number. It's possible that our array of values may contain values that are not numbers, so we'll want to ignore those values and only return the lowest number.

Here's what that might look like.

**`function** **findLowest**(values) {
    let lowestNumber = **Infinity** *// start with the highest possible number***for**(let val of values){
        **if** (isNaN(val)) {
            console.log(`not a number: **$**{val}`);
        } **else** {
            **if** (val < lowestNumber){
                lowestNumber = val
            }
        }
    }
    **return** lowestNumber;
}`

While this works, we're doing quite a bit of work in this single function. The purpose of this function is to find the lowest value in an array of values. It should not also have to worry about checking each value to see if it is not a number and doing a console.log when it does not find a valid number.

Let's break this up into two functions - one that can return `true` or `false` if a given value is a number and the other to actually find the lowest value. The second function will call the `trueIfNum` function inside of it to see if the value that is being iterated over is a number. `findLowest` does not have to worry about how to check for a number or what to do when a value that is not a number is found, it only has one responsibility - to find a the lowest value in an array of values.

**`function** **trueIfNum**(num) {
    **if** (isNaN(num)) {
        console.log(`not a number: **$**{num}`);
        **return** **false**;
    } **else** {
        **return** **true**;
    }
}

**function** **findLowest**(values) {
    let lowestNumber = **Infinity** *// start with the highest possible number***for**(let val of values){
        **if** (trueIfNum(val) && val < lowestNumber) {
            lowestNumber = val
        }
    }
    **return** lowestNumber;
}`

While this may seem like you are writing "more" lines of code, this is a much better design since it allows us to reuse our `trueIfNum` function in other parts of our code and it follows our principle of giving each function that we make a single responsibility.

As you start writing more complex functions, think about what "exactly" each function needs to do and if you find yourself doing more than just that, break your functions up into smaller functions! This idea of breaking up functions into smaller functions is commonly called **function decomposition**.

Your assignment is to write the following functions in the descriptions below - good luck!

# **Part 1**

# **`difference`**

- this function takes in two parameters and returns the difference of the two;

`difference(2,2); *// 0*
difference(0,2); *// -2*`

# **`product`**

- this function takes in two parameters and returns the product of the two;

`product(2,2); *// 4*
product(0,2); *// 0*`

# **`printDay`**

- this function takes in one parameter (a number from 1-7) and returns the day of the week (1 is Sunday, 2 is Monday, 3 is Tuesday etc.). If the number is less than 1 or greater than 7, the function should return undefined;

`printDay(4); *// "Wednesday"*
printDay(41); *// undefined*`

# **`lastElement`**

- this function takes in one parameter (an array) and returns the last value in the array. It should return `undefined` if the array is empty.

`lastElement([1,2,3,4]); *// 4*
lastElement([]); *// undefined*`

# **`numberCompare`**

- this function takes in two parameters (both numbers). If the first is greater than the second, this function returns "First is greater". If the second number is greater than the first, the function returns "Second is greater". Otherwise the function returns "Numbers are equal"

`numberCompare(1,1); *// "Numbers are equal"*
numberCompare(2,1); *// "First is greater"*
numberCompare(1,2); *// "Second is greater"*`

# **`singleLetterCount`**

- this function takes in two parameters (two strings). The first parameter should be a word and the second should be a letter. The function returns the number of times that letter appears in the word. The function should be case insensitive (does not matter if the input is lowercase or uppercase). If the letter is not found in the word, the function should return 0.

`singleLetterCount('amazing','A'); *// 2*
singleLetterCount('Rithm School','o'); *// 2*`

# **Part 2**

# **`multipleLetterCount`**

- this function takes in one parameter (a string) and returns an object with the keys being the letters and the values being the count of the letter.

`multipleLetterCount("hello"); *// {h:1, e: 1, l: 2, o:1}*
multipleLetterCount("person"); *// {p:1, e: 1, r: 1, s:1, o:1, n:1}*`

# **`arrayManipulation`**

- this function should take in at most four parameters (an array, command, location, and value).
    - If the command is "remove" and the location is "end", the function should remove the last value in the array and return the value removed. (In this case, the function only needs three arguments.)
    - If the command is "remove" and the location is "beginning", the function should remove the first value in the array and return the value removed. (In this case, the function only needs three arguments.)
    - If the command is "add" and the location is "beginning", the function should add the value (fourth parameter) to the beginning of the array and return the array.
    - If the command is "add" and the location is "end", the function should add the value (fourth parameter) to the end of the array and return the array.

`arrayManipulation([1,2,3], "remove", "end"); *// 3*
arrayManipulation([1,2,3], "remove", "beginning"); *// 1*
arrayManipulation([1,2,3], "add", "beginning", 20); *// [20,1,2,3]*
arrayManipulation([1,2,3], "add", "end", 30); *// [1,2,3,30]*`

# **`isPalindrome`**

- A Palindrome is a word, phrase, number, or other sequence of characters which reads the same backward or forward. This function should take in one parameter and returns `true` or `false` if it is a palindrome. As a bonus, allow your function to ignore whitespace and capitalization so that `isPalindrome('a man a plan a canal Panama');` returns `true`

`isPalindrome('testing'); *// false*
isPalindrome('tacocat'); *// true*
isPalindrome('hannah'); *// true*
isPalindrome('robert'); *// false*`

# **Part 3**

# **`Rock / Paper / Scissor`**

- using your knowledge so far, build a game of Rock/Paper/Scissor where through the use of the `prompt` function, a user can enter their choice and based on a random selection - they can either tie/win or lose against a computer.

# **Code**

You can find the code to all solutions [here](https://github.com/rithmschool/javascript_fundamentals_solutions/blob/master/functions_exercise/solutions.js)
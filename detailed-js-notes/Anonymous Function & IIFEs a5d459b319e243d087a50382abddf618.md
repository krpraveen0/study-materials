# Anonymous Function & IIFEs

# **Objectives**

By the end of this chapter, you should be able to:

- Create a function expression
- Write an immediately invoked function expression
- Describe some use cases for immediately invoked function expressions

# **Creating Functions: 2 Different Ways**

We mentioned earlier that there are two ways to create functions.

The first is a function declaration:

**`function** **declaredFunction**(){
    **return** "I am a function declaration!";
}`

The second is a function expression:

`let **expression** = **function**(){
    **return** "I am a function expression!";
};`

So what is the difference between these two? One difference is that when we use a function expression, we do not assign a "name" to the function. A function's name is the string of characters that come in between the `function` keyword and the set of parentheses `()`. The first function has a name, `declaredFunction`, but the second function, a function expression, does not have a name. The function without a name is called an **anonymous function**.

The second difference is a little more subtle. It has to do with how a variable gets created in your program. We will talk about the second difference in much more detail in the next chapter.

# **IIFE: Immediately Invoked Function Expressions**

An immediately invoked function expression (IIFE for short) is a function which immediately gets called after it is written. To create an IIFE, simply wrap your anonymous function in parentheses, and then call the function:

`(**function**(){
    let person = "Elie";
    **return** person;
})();`

The example defines an anonymous function that is immediately invoked. Therefore, the function executes and returns "Elie". We can even save the result of the immediately invoked function expression:

`let result = (**function**(){
    let person = "Elie";
    **return** person;
})();

console.log(result);`

(Note: the parenthesis around the function declaration are not optional! If you don't include them, you'll get a `SyntaxError`. You should verify this for yourself.)

# **IIFEs That Return Objects**

One common use case for immediately invoked function expressions is to return an object. For example, you may have an object that has information about a person:

`let personObject = (**function**() {
    **return** {
        name: "Tim",
        age: 32,
        occupation: "developer",
        hobbies: "sailing"
    };
})();`

After the code is executed, the `personObject` is equal to the object that was returned from the anonymous function. We can now use the object:

`personObject.name; *// returns "Tim"*
personObject.age; *// returns 32*
personObject.occupation; *// returns "developer"*
personObject.hobbies; *// returns "sailing"*`

Now, let's take a look at another example. This time the object will have functions for the values of the keys:

`let personObject = (**function** **invokeRightAway**(){
    let person = "Elie";
    **return** {
        **getName**: **function**(){
            **return** person;
        },
        **setName**: **function**(newName){
            person = newName;
        }
    };
})();`

Now the `personObject` we get back won't have data for each key, but rather a function that we can execute whenever we like:

`personObject.getName(); *// "Elie"*
personObject.setName("Mary"); *//*
personObject.getName(); *// "Mary"*
person; *// ReferenceError: person is not defined*`

This example highlights one use-case for IIFE's: keeping variables out of the global scope. In this case, we can still access and change the `person` variable via the `personObject.getName` and `personObject.setName` methods. However, if we try to access `person` directly from outside of the scope of `invokeRightAway`, we get a reference error.

What is pretty interesting here is that even though `invokeRightAway` finished running, we were still able to access variables from that function inside of the `getName` and `setName` methods. How is that possible? Well, through the use of something called `closure`.

# **Exercises**

- Write a function called `displayFullName`, which should accept two parameters, firstName and lastName. The function should be immediately invoked and return the firstName + lastName. You should NOT have to call this function, it should invoke right away.
- Write a function called `createCalculator`, which should return an object that has four methods, `add`, `subtract`, `multiply` and divide.

`let calc = createCalculator();
calc.add(20,20); *// 40*
calc.subtract(2,2); *// 0*
calc.multiply(2,2); *// 4*
calc.divide(12,2); *// 6*`

# **Solutions**

- `*displayFullName**`

`(**function** **displayName**(firstName, lastName){
    **return** firstName +  " " + lastName;
})('Elie', 'Schoppik')`

- `*createCalculator**`

**`function** **createCalculator**(){
    **return** {
        **add**: **function**(a,b){
            **return** a + b;
        },
        **subtract**: **function**(a,b){
            **return** a - b;
        },
        **multiply**: **function**(a,b){
            **return** a * b;
        },
        **divide**: **function**(a,b){
            **return** a / b;
        }
    }
}`
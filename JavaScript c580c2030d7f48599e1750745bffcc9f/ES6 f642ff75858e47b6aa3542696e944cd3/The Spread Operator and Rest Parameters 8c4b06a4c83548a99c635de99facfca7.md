# The Spread Operator and Rest Parameters

Rest Parameters

From time to time you might want to write a function that would take an unknown number of arguments. 

JavaScript has the ability to do this through the arguments keywords. lets take a sum() function which adds only two numbers as of now

```jsx
function sum(a,b){
    return a+b;
}
```

After some time we want this sum() function to take any number of arguments.

Here we can tell how many arguments have been passed to a function by using the `arguments` keyword. ie 

```jsx
function sum(){
	console.log(arguments);
}

let total = sum(1,2,3,4,5)
```

The above code looks great till now as it returns an array for us to work with. We can go ahead and use the reduce method to reduce the numbers

Reduce is a method that accepts a function and runs it for each value in an array. It can be used for much more than just getting the sum of some values.

```jsx
// const sum = function(){
//     //below arguments is not an array acctually it is an arrya like object
//     return arguments.reduce((pre,cur)=>{
//         return pre + cur;
//     });
// };
// const total = sum(1,2,3,4,5)
// console.log(total)
// const person={
//     fullName : 'Ajay'
// }
// function sayName(){
//     console.log(this.fullName)
// }
// //by using .call() method we can call the sayName function and set the this 
// // context to be our person object
// sayName.call(person)
// const sum=function(...numbers){
//     console.log(numbers);
// }
// function sayName(){
//     console.log(this.fullName);
// }
// sum(1,2,3,4,5,6)

// const sum = function(...args){
//     return args.reduce(function(prev,curr){
//         return prev + curr
//     });
// };

// console.log(sum(1,2,3,4,5));
//let's write a function that will take a value as the first arguments and then multipy
//the rest of the values from threre
// let multipy = function(mul,...args){
//     return args.map(function(num){
//         return mul * num;
//     });
// };

// console.log(multipy(3,14,45,6,7,8));
//Spread Operator
//syntax is same as Rest Parameters ,
//it uses ... as well
//But in spread operator we need to start with an array and then we spread it out.
// const numbers = [4,5,6,7]
// console.log(...numbers)
//Math.max() -> this method takes any number of arguments and it will return the maximum
//of them.
// const max = Math.max([1,3,4,5,6]);
// console.log(max)//NaN
//.apply() method on functions  --> this method calls a funciton and supplies for the
//this keyword as well as array that we want to use as the values of the function.

// const numbers = [1,2,3,4,5,6]
// const total = Math.max.apply(null,numbers)
// console.log(total)

// const numbers = [1,2,3,4,5,6]
// const total = Math.max(...numbers);
// console.log(total)

//using spread operator as way to concatenate arrays together
// let numberss = [1,2,3,4];
// let newNumber=[...numberss,5,6,7]
// console.log(newNumber)
```
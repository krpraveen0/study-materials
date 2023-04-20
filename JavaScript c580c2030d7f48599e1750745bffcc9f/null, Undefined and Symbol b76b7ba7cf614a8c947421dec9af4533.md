# null, Undefined and Symbol

null, undefined and symbols are primitive types in js.

**Null**

It represents an intentional absence of a primitve or composite value of a defined variable

Undefined

It represents that the value is not defined at all.

Symbol

A Symbol() is  a unique value without an associated literal.

Symbols are useful as uniques keys as Symbol() = Symbol() will return as false.

At this point let us just consider that some Symbols exists. 

```jsx
console.log(null);
console.log(undefined);
console.log(void 0);
console.log(Symbol('ES6 in practice'));
console.log(Symbol("ES6") == Symbol("ES6"));
```

in above program void is a keyword in JS which specifies that the expression next to it will not return anything.

**The let keyword**

the let keyword in JS  allows us to store data for future reference.

We can create variables with the let keyword. 

```jsx
let myDrawer;
myDrawer = 200;
```

In above code we have declared a variable with let keyword so we can think this variable like a drawer in that perspective we have created a drawer, after creating it we are putting some value(200) in our drawer . Now in order to access the value, we need to grab the handle of the box and open it. 

Now to access the 200 we need to open our drawer:

myDrawer

Initialization of let variable

The process of assigning the value for our variable for the first time is called initalization.

It can occur either in the same statement where we declared the variable( let x = 10) or after the 

declaration .

```jsx
//initalization of the variables
let x = 10 
let y ;
y = 20 
let z ;//undefined 
```

We may access a declared variable even if we have not initialized it but its value becomes undefined.

```jsx
let x = 5;
let y ;
y = x**2;
console.log(x,y,z)
let z ;
```

output

```jsx
demo.js:4 
        
       Uncaught ReferenceError: z is not defined
    at VM15 demo.js:4
```

```jsx
let x = 5;
let y ;
y = x**2;
let z ;
console.log(x,y,z)

```

output 

```jsx
5 25 undefined
```
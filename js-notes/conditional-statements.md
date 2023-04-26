# Conditional Statements

Till now we have learned 

1. primitive and composite types
2. to check the types of variables and functions
3. some of basic built-in functions 
4. some operators to perform different possible operations.

So far we can write a sequence of instructions that performs a calculations. 

In software development, there are three types of control structures:

1. **sequence**: Style of writing instructions one after the other
2. **selection**: Style of writing instructions based on conditions where either execute one set of instructions, or another one.

example:

1. **iteration**: In this style of writing instructions we execute a set of instructions a finite or infinite number of times.

As till now we have working already with sequence statements so now we will start with selection statements.

different selection statements:

if statement:

```jsx
if (condition) {
	instruction1;
	instruction2;
	----
}
```

In above program the instructions inside the if block are executed if condition is truthy.

In above program we can notice that there is a space between the if and the opening parentheses.

this space is there to indicate that if is a keyword and not a function. although this space is not a mandatory but its highly recommended .

```jsx
function printNumber(x){
 if( typeof x === 'number'){
		console.log(x + 'is a number');
	}
}
printNumber(5);
console.log(printNumber(null));
printNumber(3);
printNumber('nine')
```

In the above program we have a if block which validates the input as number but if the user is going to call the printNumber() with an argument other than number type then we haven't writtten code to handle that .

Adding another if statement:

1. if x is a number , print it
2. if x is not a number , print the message " the input has to be a number".

```jsx
function printNumber(x){
 if( typeof x === 'number'){
		console.log(x + 'is a number');
	}
if( typeof x !== 'number'){
	console.log('The input has to be number')
}
}
printNumber(3);
printNumber('three');
```

The biggest problem with the above solution is that we are writing too much for no reason.

One another problem with the above solution is lack of abstraction. Imagine that one day somebody comes and realizes that the condition typeof x === 'number' has to be modified.

If that person forget to change the second condition, then we are creating an inconsistency in our code. so here definitely we should go for another solution where we will having only one condition: 

```jsx
function printNumber(x){
 if( typeof x === 'number'){
		console.log(x + 'is a number');
	}else{
	console.log('The input has to be number')
	}
}
printNumber(3);
printNumber('three');
```

Notice the else keyword in above code . This else branch /body is only executed if the original condition is not true.

Actually we can cascade the approach further, because after the else, we can have another condition as well ie

```jsx
function logLampColor(state) {
    if (state === 1){
        console.log('Red');
    } else if( state === 2){
        console.log('Blue');
    } else if( state === 3 ){
        console.log('Green');
    } else{
        console.log('invalid state selected');
    }
}
logLampColor(3)
logLampColor('three')
```

The beauty of the above code is that we can read it as if it was a plain English.

ie

it the state is 1, then log Red, otherwise if the state is 2 then log Blue, otherwise if the state is 3 then log Green, otherwise log invalid state selected.
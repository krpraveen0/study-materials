# Objects

Preview

1. Shorthand methods
2. Shorthand properties
3. Computed properties
4. Object.assign()

Object have received some new updates in the ES6 edition of the language, including everything from new methods to updated syntax.

**Shorthand methods**

One nice addition to objects in js is the shorthand method syntax. To create an object in Js we can use this Shorthand method, we will revisit this topic when we will be learning classes in JS.

Syntax of shorthand method to create  an object

```python
let flower = {
	height : 10,
	color : 'yellow',
	grow: function(){
		this.height += 5;
	}
}
```

In the above code we have a simple flower object which has height and color and a grow method. 

When defining a method we provide a function as a value to the property on an object. In this case we are using an anonymous function. We could, if we wanted, also provide a named function.

```python
let flower = {
	height : 10,
	color : 'yellow',
	grow : function growMethod(){
		this.height +=5;
	}
}
```

The benefit of providing a named function is that we could use this name inside of our method if we need to call it recursively. With the new shorthand method syntax, we can exclude anonymous function all together.

```python
let flower = {
	height : 10,
	color : 'yellow',
	grow(){
		this.height +=5;
	}
}
```

**Shorthand Properties**

Another new feature is the ability to create object properties via a shorthand syntax.

There is not much to this, and we will see this being used later when we will be learning the destructuring concept.

Let's consider that we have some of the variables which we want to add to an object

```jsx
let firstName = "Deepak";
let lastName = "Sarkar";
let person {
	firstName : firstName,
	lastName : lastName
}
```

In above code the key in our new object will be the names of the variables we provided to it.

Now we can write the same thing using shorthand properties syntax as shown below

```jsx
let person = {firstName, lastName}
```

It really very simple to create object with new syntax which allows us to create objects from existing variables. 

A place this pattern is kind of nice is the revealing module pattern.

The idea of revealing module pattern is that you have a function, that is acting as a module that has data you want to keep private. 

From the module you return a public object that only reveals what you want to the user.

```jsx
//slider function
function slider(){
    let currentPosition = 0;
    function updatePosition(newPosition){
        currentPosition = currentPosition + newPosition;
    }
    function resetPosition(){
        currentPosition = 0;
    }
    return {
        updatePosition,
        resetPosition
    }
}
```

Above code we have a little slider module that doesn't actually do anything, but it illustrates the point. We have some private data, the currentPosition value, we also have two functions that will mutate the value. 

We expose or reveal, the functions that we want , and with the shorthand property method we can make this nice and easy as shown above.

**Computed Properties**

Computer properties is another new thing we can do with object properties in ES6.

When creating an object, properties are made up of key value pairs.

Typically a key could be a name like firstName or it could be wrapped quotes like

"firstName".

With computed properties we are able to use expression or existing variables to create keys.

```jsx
let keyName = 'firstName'
let person ={
	[keyName] : 'Deepak'
}
```

or as already mentioned, we can use expression to create keys.

```jsx
let  person= {
	['first' + 'Name'] : 'Deepak'
}
```

Object.assign()

The last thing involving objects that I want to go over is the .assign() method. 

this new method objects allows us to create copies of existing objects and also mix objects together.

The method is faily straightforward. The first argument in the method is target we want to assign, and any argument after that are sources that we want to add.

As an example, let's think about a video game. We have some base objects, like a creature, and we have different versions of these creatures.

```jsx
let bat = {
	weight: 10,
	strength: 4,
	altitude: 0,
	fly(newAltitude){
		this.altitude += newAltitude	
	}
};
```

In above program we have a base object that has some stats, now say we have a greatBat!

```jsx
let greatBat={
	weight: 15,
	strength: 7
}
```

The new bat has few new properties, but we also want it to be able to fly.

we could use inheritance via function prototypes, or we could use classes. 

Here we are going to use composition of our object. 

let's change greatBat to greaterBatProps, by making use of Object.assign() method.

```jsx
let greaterBatProps = {
	weight: 15,
	strenght: 7
};
let greaterBat = Object.assign({},bat,greaterBatProps);
console.log(greaterBat);
```

Using Object.assign() we are composing greaterBat into bat and finally into an empty object that acts as our target.

The order of our arguments matter alot, if we had called it like 

```jsx
	Object.assign({},greaterBatProps,bat)
```

We would have a whole object. However because bat came last in this example it would override anything in greaterBatProps.

Whenever you look at this Object.assign({}, arg1, arg2) you should read from the right to the left as this is how it will compose.

We can use Object.assign() method to create copies of an object.

exmple

```jsx
let person = {
	name = 'Shanti'
}
let person2 = person;
person2.name = 'Deepak'
Console.log(person2.name)
console.log(person.name)
```

We have created a person object, and gave it a simple property. Then we create a new variable called person2 and assign it to person object.

you might think that this would add a copy of the person object, but a new person object. 

However that is not the case, it just uses person as a reference, so changing the name property on person2 is going to change it on person.

Using Object.assign() we can create a copy of person in a very easy manner.

```jsx
let person = {
	name : 'Deepak'
};
let person2 = Object.assign({},person)
person2.name = 'Shanti'
console.log(person2.name) //Shanti
console.log(person.name) //Deepak
```

Note: The first argument to Object.assign() method is the target, so using blank object, we are creating a copy of the person.

```jsx
//Task
vechile ={
 engine : '',
 noDoors:  ,
 milage: ,
}
//create a car object by making use vechile object
//create a bile object by making use of car object

```
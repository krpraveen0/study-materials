# object type in JS

In JS an object is a data structure with string keys and arbitrary values.

We can imagine it like a machine that accepts a key and gives a value.

Some people call this data structure as associative array , others call it as hashmap.

NOte: Symbol keys are not allowed for strings. more later

```jsx
//creating an object 
let author = {
	name:null,
	website: "engineeringcoders.com",
	age: 2
}

//accessing the values of an object 
author.name = 'vidya';
console.log(author.name,author["website"])

//deleting a value of an object 
delete author.name
console.log(author.name,author["website"])
console.log("Authon name",author.name)

```

A field in an object can be reference in two ways :

1. using dot notation: object_name.member_name
2. using brackets(associative array) notation: object_name['member_name']

WE can delete a value in an object by using delete operator in another word it deletes a field of an object 

If a field in an object is deleted or not even declared, then the value of this field is undefined.
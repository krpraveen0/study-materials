# Arrow Function

```python
//coffescript
// add = (a,b) ->
//     a+b

//ES6-- Arrow function 
// const add = (a,b) =>{
//     return a+b
// }

// console.log(add(4,5))

//arrow function as an anonymous function
// const add = (a,b)=> {
//     return a+b;
// }
//arrow function in a single line
// const add = (a,b) => a + b
// add(2,3)

//making functional patterns using arrow function
// const numbers = [1,2,3,4,5,6];
// const doubled = numbers.map((n)=>{return n*2});
// console.log(doubled)

//this keyword
// const person={
//     name : 'Ajay',
// //     sayName(){
// //         console.log(`Hi I am ${this.name}`)
// //     }
//     sayName : () =>{
//         console.log(`Hi I am ${this.name}`)
//     }
// }

// person.sayName();

// const person ={
//     name: 'Ajay',
//     hobbies:['Cricket','movies','Gaming'],
//     showHobbies: function(){
//         this.hobbies.forEach(hobby=> console.log(`${this.name} likes ${hobby}`))
//     }
// }

// person.showHobbies();

//Binding of an arrrow function
// const person = {
//     city : 'Mysuru',
// }

// const sayName =()=>{console.log(this.city)};

// sayName.call(person)

//note : inside of an arrow function there is no access to the arguments keyword.
```
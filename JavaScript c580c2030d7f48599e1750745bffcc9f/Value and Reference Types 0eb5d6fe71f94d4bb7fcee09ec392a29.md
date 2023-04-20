# Value and Reference Types

Whenever we code in Javascript it doesn't gives us full access to its data structures in the memory.

However reference types still exists in the language. Mixing value and reference types comes with unwanted side-effects and bugs. 

So understanding the difference between values and reference types plays a vital role in writing robust program.

Numbers, Booleans, strings, null and undefined are primitive types. All primitive types are passed by value. Objects, arrays and functions are passed by reference.

In javascript strings are somewhat special as it is not defined as array of characters (as in other programming languages like python, java, c++etc) .

Even the character type doesn't exists in Javascript.

In Javascript strings are immutable data types, with an interface that makes them look like an array of characters. In practice if we modify some string then it results in a new immutable string value. ie

![string-immutability.png](Value%20and%20Reference%20Types%200eb5d6fe71f94d4bb7fcee09ec392a29/string-immutability.png)

AS show in above program we have tried to modify the name string from vidya to sagar but instead of modifing the existing value it create a new string and start referencing to it.

```python
//creating an array of objects with a reference variable
var people = [
    {name: 'Vidya', age : 78},
    {name: 'Sagar', age : 87}
];

var getInitials = function(name) {
    name = name.split(' ').map(function (word) {
        return word.charAt(0)
    }).join('')
    return name
    
}

//creating a function to increase the age of the persons by 1
var increaseAge = function (person) {
    person.age += 1;
}

//adding more person to that array
var addPerson = function (person,name,age) {
    person.push({name:name,age:age})
    
}

//driver code
//Part1: getInitials
console.log(getInitials(people[0].name))
console.log(people[0].name);

//Part2: increasing the persons age
increaseAge(people[1]);
console.log(people[1].age)

//Part3: adding some more Peoples in Person array
addPerson(people, "praveen kumar", '25');
console.log(people);
```

In above code

In the first part, the initials of  a name are constructed by the getInitials function.

Here the string value passed to the function is copied. this copy is accessed and modified inside the function. These modifications have nothing to do with the original value at people[0].name.

In second part the increaseAge function accepts an object. As objects are reference types, only the reference to the passed person is copied. When members of the referenced object is changed, the changes are kept even after the executing the function. these changes are accessible via each references.

what is the difference between the value and reference.
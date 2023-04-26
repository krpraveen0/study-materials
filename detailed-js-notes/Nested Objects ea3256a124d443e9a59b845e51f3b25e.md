# Nested Objects

# **Objectives:**

By the end of this chapter, you should be able to:

- Create nested data structures using objects
- Access and iterate over data in a nested data structure
- Add and remove data inside of a complex data structure

# **What is a data structure? A nested one?**

So what do we mean by data structure? In some sense, a data structure is just that: a way of structuring data. In computer science, there are a multitude of different data structures (as you'll see!), because the most efficient way to store data depends on how you intend to *use* the data. Do you just need to read the data, or do you need to update it? How large is your set of data, and how quickly do you need to find things in it? Questions like these greatly influence what type of data structure you should be using.

For now, though, we'll keep things limited to `Objects` and `Arrays`. We've already seen how to use both of these structures to organize data. As we'll see in this unit, even with just these two data structures, we can get pretty far in terms of storing and accessing complex data.

What, then, is a nested data structure? It just means one data structure inside of another! Let's start with a simple example.

# **Objects within Objects**

Below is a simple example of creating an object that has a key and the value for that key is another object:

`let schools = {
    georgiaInstituteOfTechnology: {
        address: "North Ave NW, Atlanta, GA 30332",
        phoneNumber: "(404) 894-2000",
        dateEstablished: "October 13, 1885"
    }
};`

Now to access an object within an object, we can use dot notation just like in objects that are not nested:

*`// This statement assigns the object that is nested inside// of the larger schools object to the gtObject variable.*
let gtObject = schools.georgiaInstituteOfTechnology;`

Now that we have the `gtObject` variable, we can use it to access keys within that object:

`gtObject.address; *// returns "North Ave NW, Atlanta, GA 30332"*
gtObject.phoneNumber; *// returns "(404) 894-2000"*
gtObject.dateEstablished; *//returns "October 13, 1885"*`

In fact, we don't even need the intermediate `gtObject` variable. We can simply use the dot operater on the first statement like this:

`schools.georgiaInstituteOfTechnology.address;
schools.georgiaInstituteOfTechnology.phoneNumber;
schools.georgiaInstituteOfTechnology.dateEstablished;`

All of the above statements evaluate to the same values as the `gtObject` examples.

# **Arrays Within Objects**

Now let's look at an example of an object with an array as the value:

`let instructorData = {
    name: "Tim",
    favoriteHobbies: ["Sailing", "Hiking", "Coding"]
};`

In this example we now have multiple keys. The `name` key has a simple value of a string, `"Tim"`, but the `favoriteHobbies` key has a more complex value which is an array.

Just like in the objects within objects example, we can access an element in the array by using the dot notation, and then access the array normally. To get the first element in the array, the code would be as follows:

`instructorData.favoriteHobbies[0]; *// returns "Sailing"*`

How would you add another hobby to the `favoriteHobbies` array inside of the object?

# **Complex Objects**

Now let's look at an example that combines objects and arrays:

`let instructorData = {
    name: "Elie",
    additionalData: {
        instructor: **true**,
        favoriteHobbies: ["Playing Cello", "Tennis", "Coding"],
        moreDetails: {
            favoriteBasketballTeam: "New York Knicks",
            numberOfSiblings: 3,
            isYoungest: **true**,
            hometown: {
                city: "West Orange",
                state: "NJ",
            },
            citiesLivedIn: ["Seattle", "Providence", "New York"]
        }
    }
};

instructorData.name; *// "Elie"*
instructorData.additionalData.instructor; *// true*
instructorData.additionalData.favoriteHobbies[2]; *// "Coding"*
instructorData.additionalData.moreDetails.favoriteBasketballTeam; *// "New York Knicks"*
instructorData.additionalData.moreDetails.hometown.state; *// "NJ"*
instructorData.additionalData.moreDetails.citiesLivedIn[1]; *// "Providence"*`

So you may be thinking, *am I really going to be working with data like this? Seriously?* The answer is a strong **YES**! Very commonly, when you receive large amounts of data from third parties, you will be given it in a format that includes nested objects and/or arrays. It is imperative that you understand how to access data in these nested data structures. If you can't get to a point where you can easily manipulate nested data structures, you'll have a very difficult time integrating any kind of outside data into the applications you'll be building later on. Copy and paste the previous example into a snippet or make up your own example to practice!

# **Accessing and Setting values in nested objects**

Using the dot notation is a great way to access values in nested objects. However, when dynamically setting values in a nested object (when you don't know exactly what the name of the key is going to be), you have to use the bracket notation. Let's take a look at a quick example. In the example below, we'd like to write a function that adds a key to the nested object

`let programmingLanguages = {
    java: {
        yearCreated: 1995,
        creator: "James Gosling"
    },
    javaScript: {
        yearCreated: 1995,
        creator: "Brendan Eich"
    }
}

**function** **addProgrammingLanguage**(nameOfLanguage, yearLanguageCreated, creatorOfLanguage){
    *// how can we access the programming languages object?// We can't use dot notation, because we don't know the name of// the key until the function is called.// Instead we use bracket notation where the key is the// nameOfLanguage that is being passed to the function.*
    programmingLanguages[nameOfLanguage] = {
        *// Creating the object which will be the value of the// key.  We can directly assign the yearLanguageCreated// and creatorOfLanguage to the appropriate keys here.*yearCreated: yearLanguageCreated,
        creator: creatorOfLanguage
    }
}

*// Usage example: Adding a key of ruby to the programming language object,// with the value of 1995 for the key "yearCreated" and the value// "Yukihiro Matsumoto" for creatorOfLanguage*
addProgrammingLanguage("ruby", 1995, "Yukihiro Matsumoto");`

Remember, that when adding keys to an object, if you do NOT know exactly what the name of the key will be (meaning that the key will be dynamically created), you HAVE to use the bracket notation.

# **Writing functions to produce values in a nested data structure**

When you're interacting with a nested data structure, sometimes it's helpful to encapsulate some of your logic into a function. This is especially true if you'll need to manipulate the data structure in similar ways multiple times. Below are some examples of writing functions that interact with nested data structures in different ways. We'll start with the same `instructorData` example from before:

`let instructorData = {
    name: "Elie",
    additionalData: {
        instructor: **true**,
        favoriteHobbies: ["Playing Cello", "Tennis", "Coding"],
        moreDetails: {
            favoriteBasketballTeam: "New York Knicks",
            numberOfSiblings: 3,
            isYoungest: **true**,
            hometown: {
                city: "West Orange",
                state: "NJ",
            },
            citiesLivedIn: ["Seattle", "Providence", "New York"]
        }
    }
};`

Now let's try to write some functions that operate on this nested data structure. The answers are below - but try to do these on your own first!

# **Exercises**

Write a function called `displayCities` that console.logs all the values in the citiesLivedIn array:

`displayCities();

*// "Seattle"// "Providence"// "New York"*`

Write a function called `displayHometownData` that console.logs all the values inside of the `hometown` object

`displayHometownData();

*// "West Orange"// "NJ"*`

Let's write a function called `addDetail` that accepts two parameters, a key and a value and adds the key and value to the `moreDetails` object and returns the `moreDetails` object

`addDetail("isHilarious", **true**);
*/*
{
    favoriteBasketballTeam: "New York Knicks",
    numberOfSiblings: 3,
    isYoungest: true,
    hometown: {
        city: "West Orange",
        state: "NJ",
    },
    citiesLivedIn: ["Seattle", "Providence", "New York"],
    isHilarious: true
}
*/*
addDetail("previousApartments", ["Mission", "North Beach", "Nob Hill"]);
*/*
{
    favoriteBasketballTeam: "New York Knicks",
    numberOfSiblings: 3,
    isYoungest: true,
    hometown: {
        city: "West Orange",
        state: "NJ",
    },
    citiesLivedIn: ["Seattle", "Providence", "New York"],
    isHilarious: true
    previousApartments: ["Mission", "North Beach", "Nob Hill"]
}
*/*`

Finally, let's write a function called `removeDetail` that removes a key in the `moreDetails` object and returns the `moreDetails` object (the new keys added above are not included in these examples).

`removeDetail('citiesLivedIn');
*/*
{
    favoriteBasketballTeam: "New York Knicks",
    numberOfSiblings: 3,
    isYoungest: true,
    hometown: {
        city: "West Orange",
        state: "NJ",
    }
}
*/*
removeDetail('hometown');
*/*
{
    favoriteBasketballTeam: "New York Knicks",
    numberOfSiblings: 3,
    isYoungest: true
}
*/*
removeDetail('favoriteBasketballTeam');
*/*
{
    numberOfSiblings: 3,
    isYoungest: true
}
*/*`

# **Solutions**

For most of these functions, it is useful to store the nested information in a variable to avoid having to type it multiple times. Here are the solutions to the previous problems:

**displayCities**

**`function** **displayCities**(){
    let cityArray = instructorData.additionalData.moreDetails.citiesLivedIn;
    **for**(let i=0; i< cityArray.length; i++){
        console.log(cityArray[i]);
    }
}`

**displayHometownData**

**`function** **displayHometownData**(){
    let hometownObject = instructorData.additionalData.moreDetails.hometown;
    **for**(let key **in** hometownObject){
        console.log(hometownObject[key]);
    }
}`

**addDetail**

**`function** **addDetail**(key,value){
    let detailsObject = instructorData.additionalData.moreDetails;
    detailsObject[key] = value;
    **return** detailsObject;
}`

**removeDetail**

We need to make sure we use the bracket notation and not dot notation when accessing our object. Since we do not know the name of the key until the function is called, we need to dynamically access that key, which must be done using bracket notation.

**`function** **removeDetail**(key){
    let detailsObject = instructorData.additionalData.moreDetails;
    let valueToBeRemoved = detailsObject[key];
    **delete** detailsObject[key];
    **return** detailsObject;
}`

Given the following nested object:

`let nestedData = {
  innerData: {
    order: ["first", "second", "third"],
    snacks: ["chips", "fruit", "crackers"],
    numberData: {
        primeNumbers: [2,3,5,7,11],
        fibonnaci: [1,1,2,3,5,8,13]
    },
    **addSnack**: **function**(snack){
        this.snacks.push(snack);
        **return** this;
    }
  }
}`

- Using a for loop, console.log all of the numbers in the `primeNumbers` array.
- Using a for loop, console.log all of the even Fibonnaci numbers.
- Console.log the value "second" inside the order array.
- Invoke the `addSnack` function and add the snack "chocolate".
- Inside of the addSnack function there is a special keyword called `this`. What does the word `this` refer to inside the `addSnack` function?

Given the following nested object:

`let nestedObject = {
  speakers: [{name:"Elie"},{name:"Tim"},{name:"Matt"}],
  data: {
    continents: {
      europe: {
        countries: {
          switzerland: {
            capital: "Bern",
            population: 8000000
          }
        }
      }
    },
    languages: {
      spanish: {
          hello: "Hola"
      },
      french: {
          hello: "Bonjour"
      }
    }
  }
}`

- Write a function `addSpeaker` to add a speaker to the array of speakers. The speaker you add must be an object with a key of name and a value of whatever you'd like.
- Write a function `addLanguage` that adds a language to the languages object. The language object you add should have a key with the name of the language and the value of another object with a key of "hello" and a value of however you spell "hello" in the language you add.
- Write a function `addCountry` that adds a European country to the countries object (inside of the continents object, inside of the countries object). The country you add should be an object with the key as name of the country and the value as an object with the keys of "capital" and "population" and their respective values.

# **Objectives:**

By the end of this chapter, you should be able to:

- Create and access values in two dimensional arrays
- Understand real-world use cases of multidimensial arrays
- Iterate over data in a multidimensional array

# **Multidimensional Arrays**

Multidimensional arrays are a special kind of nested data structure, which consists of an array, each of whose elements is again an array. Here's an example:

`let myFirstSubarray = [["this", "is"], ["super", "cool"]];`

When working with two-dimensional arrays, if you want to print out all of the values, you are going to need a loop inside of a loop! Let's examine this a bit further.

`let nestedArr = [[1, 2], [3, 4]];
**for** (let i = 0; i < nestedArr.length; i++) {
  console.log(nestedArr[i]);
}

*// this will log out...// [1,2]// [3,4]*`

But what if we want to print out each individual value (i.e. 1, 2, 3, 4), and not just each array? We will need another loop inside of the first loop! We traditionally initialize the inner counter as `j` (the letter that comes after `i`) and we will loop as long as `j` is less than the length of **each** inner array.

`let nestedArr = [[1, 2], [3, 4]];
**for** (let i = 0; i < nestedArr.length; i++) {
  **for** (let j = 0; j < nestedArr[i].length; j++) {
    *// notice that we are going inside the outer array// and now inside of the inner array*
    console.log(nestedArr[i][j]);
  }
}

*// this will log out...// 1// 2// 3// 4*`

Here is an another example - take a quick look and try to replicate it without looking at the code!

`let nestedArr = [[1, 2, 3], [4, 5, 6], [7, 8, 9, 10, 11, 12]];
**for** (let i = 0; i < nestedArr.length; i++) {
  **for** (let j = 0; j < nestedArr[i].length; j++) {
    console.log(nestedArr[i][j]);
  }
}`

So when are two-dimensional arrays used? Quite often! For example, when building games you can often model the game board like a nested array. You can use a nested array for a tic-tac-toe board, a Minesweeper board or maybe for a couple hands of poker!

# **Additional Resources**

An excellent post on accessing nested resources - [http://stackoverflow.com/questions/11922383/access-process-nested-objects-arrays-or-json](https://stackoverflow.com/questions/11922383/access-process-nested-objects-arrays-or-json)

# **Exercises**

Given the following array, write a function called `printEvens` that console.logs all of the even numbers

`let nestedArr = [[1, 2, 3], [4, 5, 6], [7, 8], [9, 10, 11, 12]];

printEvens();

*// 2// 4// 6// 8// 10// 12*`

Given the following array, write a function called `sumTotal` returns the sum of all numbers in the array

`let nestedArr = [[1, 2], [3, 4], [5, 6]];

sumTotal(); *// 21*`

Here's what a solution might look like for the `sumTotal` function:

**`function** **sumTotal**() {
  let total = 0;
  **for** (let i = 0; i < nestedArr.length; i++) {
    **for** (let j = 0; j < nestedArr[i].length; j++) {
      total += nestedArr[i][j];
    }
  }
  **return** total;
}`

**Optional Bonus**

Given the following array, write a function called `countVowels`, which returns the count of all of the vowels in each string regardless of case. To see if a value is an array, you can **not** use `typeof` since that will return `'object'`, so one way to do this is by using the `Array.isArray` function.

`let arr = [];
Array.isArray(arr); *// true*
Array.isArray("Hello"); *// false*

let nestedArr = [
  "Elie",
  ["Matt", ["Tim"]],
  ["Colt", ["Whiskey", ["Janey"], "Tom"]],
  "Lorien"
];

countVowels(); *// 14*`

# **Optional Bonus Solution**

Here is a solution using iteration, as you continue to learn more about programming, you'll see that this is an excellent use case for recursion (writing a function that calls itself).

**`function** **seeIfVowel**(**char**, count) {
  let vowels = "aeiou";
  **if** (vowels.includes(**char**.toLowerCase())) {
    **return** ++count; *// add 1 to count then return the value (this is called a prefix operator)*
  }
  **return** count;
}

**function** **countCharacters**(str, count) {
  **for** (let i = 0; i < str.length; i++) {
    count = seeIfVowel(str[i], count);
  }
  **return** count;
}

**function** **countVowels**(arr) {
  let count = 0;
  **for** (let i = 0; i < arr.length; i++) {
    **if** (Array.isArray(arr[i])) {
      **for** (let j = 0; j < arr[i].length; j++) {
        **if** (Array.isArray(arr[i][j])) {
          **for** (let k = 0; k < arr[i][j].length; k++) {
            **if** (Array.isArray(arr[i][j][k])) {
              **for** (let l = 0; l < arr[i][j][k].length; l++) {
                count = countCharacters(arr[i][j][k][l], count);
              }
            } **else** {
              count = countCharacters(arr[i][j][k], count);
            }
          }
        } **else** {
          count = countCharacters(arr[i][j], count);
        }
      }
    } **else** {
      count = countCharacters(arr[i], count);
    }
  }
  **return** count;
}

**function** **countVowelsEasier**(arr) {
  let str = arr.toString();
  let count = 0;
  count = countCharacters(str, count);
  **return** count;
}`

- Write a function called `rotate` which takes an array and a number, and moves each element however many spaces the number is to the right. For the value at the end of the array, `rotate` should move it back to the beginning.

`rotate([1,2,3], 1) *// [3,1,2]*
rotate([1,2,3], 2) *// [2,3,1]*
rotate([1,2,3], 3) *// [1,2,3]*`

- Write a function called `makeXOGrid` which takes in two parameters, rows and columns, and returns an array of arrays with the number of values in each subarray equal to the `columns` parameter and the number of subarrays equal to the `rows` parameter. The values in the sub-arrays should switch between `"X"` and `"O"`.

`makeXOGrid(1,4) 

*/*/
[["X","O","X","O"]]
/*/*

makeXOGrid(3,2) 

*/*/
[["X","O"],["X","O"],["X","O"]]
/*/*

makeXOGrid(3,3) 
*/*/
[["X","O","X"],["O","X","O"],["X","O","X"]]
/*/*`

# **Solutions**

You can find solutions to the exercises [here](https://github.com/rithmschool/intermediate_javascript_solutions/blob/master/nested_arrays_exercise/solution.js)
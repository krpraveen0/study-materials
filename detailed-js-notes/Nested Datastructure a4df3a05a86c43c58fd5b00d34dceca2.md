# Nested Datastructure

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
        nestedData.innerData.snacks.push(snack);
        **return** nestedData.innerData.snacks;
    }
  }
}`

- Using a for loop, console.log all of the numbers in the `primeNumbers` array.
- Using a for loop, console.log all of the even Fibonnaci numbers.
- Console.log the value "second" inside the order array.
- Invoke the `addSnack` function and add the snack "chocolate".

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

# **Solutions**

You can find solutions to the exercises [here](https://github.com/rithmschool/intermediate_javascript_solutions/blob/master/nested_objects_exercise/solution.js)
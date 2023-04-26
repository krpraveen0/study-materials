# Default Parameters

Default Parameters are great addition to the language. They allow us to well, add default parameter.

Lets consider the given example below where we have created a simple function to get data from the source.

```jsx
//simple function to get data from the source
function getData(url){
    url = url || 'http://api.data.com'
    return fetch(url)
    .then(res => res.json);
}
```

In the above code if a url is passed in, it will go and get the data from that URL.

However if no url is provided, it will get the data from `[http://api.data.com](http://api.data.com)` , which is a default source.

Now with ES6 we can specify the default parameter while passing the arguments in the function definition which makes it more apparent what is exactly happening .

```jsx
function getData(url = 'http://api.data.com'){
    return fetch(url)
        .then(res=>res.json())
}
getData()
getData('https://www.engineeringcoders.com')
```

The above code really cleans things up. With the ability to create Default Params, we can have more flexible and reliable functions.

Working of the default param function:

The way default params works is that if nothing is passed in it, will take the value stored in the function definition, in this case url=’http://api.data.com’. 

If we don pass in a value for that position it will override the section.

When working with the default params we are able to mix and match, allowing us to create easy-to-understand optional parameters for our funcitons.

```jsx
function dataHandler(method,url='http://api.data.com'){
    return fetch(url)
    .then(res => res.json);
}

//calling the dataHandler with POST method to endpoint http://api.data.com
dataHandler('POST')
//calling the dataHandler with GET method to endpoint http://api.data.com
dataHandler('GET')
```
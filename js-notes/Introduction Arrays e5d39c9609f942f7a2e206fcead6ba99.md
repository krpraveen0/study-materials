# Introduction Arrays

An array is an ordered list of items arranged in a contiguous manner where the items may be of any data type.

An array has a continuous keys by using which we can access different items in an array.

for example:

creating an array

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
let storage = [1,'monday',null]
```

accessing the elements of an array

Each element of an array can be accessed by using an index starting from zero till length of array- 1.

ie

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
console.log(days[0])
```

If we will try to access an element of an array which is not there then we will get undefined

```jsx
console.log(days[7])
```

output

```jsx
undefined
```

How long is an array?

WE can find the length of an array by using a property over array called length ie

```jsx
console.log(days.length)
```

output

```jsx
7
```

Adding and Removing element in an array

Adding elements to an array to the beginning or end:

We can add elements to the beginning and to the end of the array 

1. By using push() - it adds elements to the end of an array.
2. By using unshift() - it adds elements to the beginning of an array.

example:

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
days.push('Saturday');
console.log("Saturday is added is at the end of the array",days)
days.unshift("Monday");
console.log("Monday is added at the beginning of the array",days)
```

output

```jsx
Saturday is added is at the end of the array (8) ['monday', 'tuesday', 'wednesday', 'thursday', 'friday', 'saturday', 'sunday', 'Saturday']
Monday is added at the beginning of the array (9) ['Monday', 'monday', 'tuesday', 'wednesday', 'thursday', 'friday', 'saturday', 'sunday', 'Saturday']
```

Removing an element from an array

We can remove an element from an array by using following two methods:

1. By using pop() : it removes the last element of an array and returns it.
2. By using shift() : it removes the first element of an array and returns it.

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
days.pop();
console.log("the last item of the array ie sunday will be removed",days)
days.shift();
console.log("The first item of the array ie monday will be removed",days)
```

output

```jsx
the last item of the array ie sunday will be removed (6) ['monday', 'tuesday', 'wednesday', 'thursday', 'friday', 'saturday']
demo.js:5 The first item of the array ie monday will be removed (5) ['tuesday', 'wednesday', 'thursday', 'friday', 'saturday']
```

**How to delete any item of an array** 

We can delete any element of an array by using delete keyword  and the index of the element.  After deleting that element the value undefined will be placed in the place of deleted item

example:

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
delete days[1]
console.log('The array after deleting the days[1] item',days)
console.log(days[1])
```

output:

```jsx
The array after deleting the days[1] item (7) ['monday', empty, 'wednesday', 'thursday', 'friday', 'saturday', 'sunday']
0: "monday"2: "wednesday"3: "thursday"4: "friday"5: "saturday"6: "sunday"length: 7[[Prototype]]: Array(0)
class8.js:4 undefined
```

How to overwrite and add elements at any index of an array

The values of an array can be set by using their indices, and equating them to a new value.

WE can overwrite the existing values, or add new values to the array . The indices of the added values do not have to be continuous:

```jsx
let days = ['monday','tuesday','wednesday','thursday','friday','saturday','sunday']
days[1] ='sunday'
console.log(days);
days[9] = 'freeday'
console.log(days)
```

output:

```jsx
(7) ['monday', 'sunday', 'wednesday', 'thursday', 'friday', 'saturday', 'sunday']
class8.js:5 
(10) ['monday', 'sunday', 'wednesday', 'thursday', 'friday', 'saturday', 'sunday', empty × 2, 'freeday']
0: "monday"
1: "sunday"
2: "wednesday"
3: "thursday"
4: "friday"
5: "saturday"
6: "sunday"
9: "freeday"
length: 10
[[Prototype]]: Array(0)
```

Task:

Suppose there is an array give below

```jsx
array = [7,15,32,9,'3','11',2]
```

Determine the output printed to the javascript console.

1. console.log(array[3])

```jsx
9
```

1. console.log(array[7]);

```jsx
undefined
```

1. console.log(array.pop())

```jsx
2
```

1. console.log(array)

```jsx
whole array
```

1. console.log(array.shift())

```jsx
removes first element of an array ie 7
```

1. console.log(array)

```jsx

```

1. console.log(array.push(6))

```jsx
adds 6 at the end of the array
```

1. console.log(array)

Summary

```jsx
array = [7,15,32,9,'3','11',2]
console.log(array[3])
console.log(array[7])
console.log(array.pop())
console.log(array)
console.log(array.shift())
console.log(array)
console.log(array.push(6))
console.log(array)
console.log(array.unshift(7))
```
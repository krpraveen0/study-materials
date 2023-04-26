# JavaScript nested array

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

Here is an another example - take a quick look and try to figure out what it will log without running the code!

`let nestedArr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9, 10, 11, 12]
];

**for** (let i = 0; i < nestedArr.length; i++) {
  **for** (let j = 0; j < nestedArr[i].length; j++) {
    console.log(nestedArr[i][j]);
  }
}`

# **Using a for...of loop**

It's often easier to use a `for...of` loop to iterate over nested arrays so that you can create well defined variable names for the data you iterate over. If you don't need the index in an array, favor using a `for..of` loop!

`let nestedArr = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9, 10, 11, 12]
];

**for** (let row of nestedArray){
  **for** (let cell of row){
    console.log(cell);
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
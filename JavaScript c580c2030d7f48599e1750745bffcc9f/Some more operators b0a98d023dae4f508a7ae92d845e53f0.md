# Some more operators

In very soon time we are going to start loops and conditional statements. There are some operators which really helps alot working in those conditional and looping statements.

1. compound operator: 
    1. += 
    2. -=
    3. *=
    4. /=
    5. %=

Here in all above compound operators first the arithmetic operations are performed and after that assignment operation is performed .

example:

 

```jsx
//sum +=1 is evaluated to sum = sum + 1
sum = 0
console.log(sum)
sum +=1;//sum = sum + 1
console.log(sum)
```

1. increment operator :
    1. post increment operator( variable-name ++) : it returns the original value of variable, then increases its value by 1.
    
     ie x++ 
    
    1. pre increment operator( ++ variable-name) : It increases the value of variable by 1 and then returns the increased value.
    
    ie ++x
    
2. decrement operator 
    1. post decrement operator( variable-name —): It returns the original value of the variable, then decreases its value by 1.
    2. pre decrement operator( — variable-name): It decreases the variable value by 1, then it returns the decreased value.
    
    example: 
    
    ```jsx
    x = 10 ;
    //post increment 
    console.log("post increment",x++);//10 
    //pre increment
    console.log("pre increment",++x)//12
    //pre decrement 
    console.log("pre decrement",--x)//
    //post decrement
    console.log("post decrement",x--)//
    ```
    
    Note:
    
    x++ executes the statement and then increments the value.
    
    ++x increments the  value and then executes the statment.
    
    Logical Operators:
    
     There are three logical operators:
    
    1. and operator (&&)
    
    The and operator is a binary operator which takes two operands to perform a logical operation in which if both the operands are evaluated to true then only it returns true otherwise it returns false. ie 
    
    example:
    
    ```jsx
    function isNotEmptyArray(x){
    	return Array.isArray(x)  && x.lenght > 0 ;
    }
    console.log(isNotEmptyArray(5))
    console.log(isNotEmptyArray([]))
    console.log(isNotEmptyArray([2])
    ```
    
    1. or operator (||)
    
    The or operator is a binary operator which takes two operands to perform a logical operation in which if any one of the operands evaluate to true then it returns true otherwise it returns [false.ie](http://false.ie) 
    
    example:
    
    ```jsx
    function numerofString(x){
    	return type of x === 'number' || typeof x === 'string'
    }
    
    console.log(numberofString(NaN));
    console.log(numberofString(''));
    console.log(numberofString(null));
    ```
    
    1. not operator( !)
    
    The not operator is a unary operator which takes one operand to perform a logical operation in which it return the complement the given operand. ie
    
    ```jsx
    ! true = false
    ! false = true
    ```
    
    How to check for NaN value?
    
    to check if a value is NaN or not we have a function isNaN() inside Number object
    
    ie
    
    ```jsx
    console.log(Number.isNaN(NaN))
    ```
    
     The problem with NaN is that when we compare NaN with NaN then it returns false.
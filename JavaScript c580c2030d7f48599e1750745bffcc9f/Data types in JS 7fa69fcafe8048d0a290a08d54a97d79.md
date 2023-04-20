# Data types in JS

There are six primitive data types in Javascript

1. boolean(true or false)
2. number( includes integer, floating point numbe(0.9,7.8 etc) )
3. string( 'sagar' , "vidya" )
4. null type(denoted by null)
5. undefined(denoted by undefined)
6. symbol

**Operators in JS:**

![operator-1.png](Data%20types%20in%20JS%207fa69fcafe8048d0a290a08d54a97d79/operator-1.png)

Classification of the operators on the basis of number of operands

![classification of the operators.png](Data%20types%20in%20JS%207fa69fcafe8048d0a290a08d54a97d79/classification_of_the_operators.png)

comparison and ternary Operators

Comparison operators or realtional operators

1. >
2. <
3. ≥
4. ≤
5. ==
6. ===

example:

```jsx
var num1 = 5
var num2 = 4
alert(num2>num1)//False
alert(num2<num1)//True
alert(num2 == num1)//False
```

difference between == and ===

```jsx
var num3 = 56
var num4 = '56'
alert(num3 == num4)//check for only value
alert(num3 === num4)//checks for value and type
```

Ternary operator

![ternary-operator.png](Data%20types%20in%20JS%207fa69fcafe8048d0a290a08d54a97d79/ternary-operator.png)

In above picture as we can that ternary operator takes three operands and the operation depends upon the first operand which is condition so based on this condition operand the other one of the two operands will be executed.

If condition evaluates to true then code a is going to be executed

If condition evaluates to false then code b is going to be executed.
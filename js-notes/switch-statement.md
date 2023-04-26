# switch statement

switch statement is a way of executing selective instructions .

switch is an operator which is an abbreviated version for a long chain of if-else statements.

```jsx
function logLampColor(state) {
    switch(state){
        case 1:
            console.log('Red');
            break;
        case 2:
            console.log('Blue');
            break;
        case 3:
            console.log('Green');
            break;
        case 4:
            console.log('Yellow');
            break;
        default:
            console.log('invalid input given');
    }
}

logLampColor(3);
logLampColor('three');
logLampColor(4);
```

In above code we have a variable inside the switch(). This variable may have values. We jump to the case label for which state is equal to the label value. then we start executing the code .

In above code we have used break statements .

Why the break statement is so important in above program?

I
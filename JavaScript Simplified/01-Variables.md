A variable is like a box, a box can store anything in it and it can be moved from one place to another and can also be given to others. It can have a name that can be used to reference it. 

A variable named shoes can contain a list of all the shoes you own or the shoes that you want to buy. In JavaScript, we can use the following pre-defined keywords to create a variable which includes `let, var,` and `const`.

```jsx
let name = "Sam"
let age = 12
const pi = 3.14
```

Variable names should be easy to read and understand and the first character of a variable name be an alphabet or a special character like the `@` sign. Variable names cannot be started by a number but can include them after the first character.

>[!NOTE]
>Before ES6 there was only one way to declare variables in JavaScript, that was by using the `var` keyword. ES6 introduced two new ways to declare variables in JavaScript called `let` and `const` making the total ways to declare a variable to three.

- Vars can be hoisted in the global scope and that is the reason they were replaced with let.
- Lets cannot be hoisted globally and work only inside their own scope.
- Consts values cannot be changed down the line once assigned.

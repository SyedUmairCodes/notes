JavaScript allows us to assign different types of data to a variable. Variables can hold numerical, alphanumerical, and floating point numbers as data types in JavaScript.

```JS
let name = "David"
let age = 14
let username = "Daiv404"
const pi = 3.14
```

> [!IMPORTANT]
> If you don't know the data type of a variable you can use the `typeof` function to check it's current data type.

```jsx
let a = 1
console.log(typeOf a)
```

>[!IMPORTANT]
>In JavaScript numbers are very different than other programming languages such as C# or Python. In JavaScript whole numbers or numbers with a floating-point are called numbers while in other languages they are denoted by the **Integer and Float** data type respectively.

```jsx
let a = 123 //This is a number in JS
let b = 1.3445 //This is also a number in JS
```

When you want to write text in JavaScript you use the **String** data type. But JavaScript won't understand your text if you just type it out instead you will have to type your text between single or double-quotes.

```jsx
let my_name = Jhon //This is not considered as a string
let full_name = "Jhon Doe" //This will be considered as a string
```

We can also put a string inside of another string, the solution is that you write the first text in single quotes and then write the second text in double quotes inside the single quotes. 

```jsx
let greeting = 'Hello, my name is "Jhon".'
```

---
Booleans are another data type in JavaScript and other programming languages that take only two values, either `true` or `false`. 

> [!IMPORTANT]
> Booleans are different from strings and numbers because you cannot use a variable that is a Boolean like a string or a number.

```jsx
let a = true
let b = false
```

>[!NOTE]
>We use special operators to perform operations on Booleans called the **AND and OR** operators denoted by the **&& and ||** symbols respectively.

```jsx
let a = true
let b = false

console.log(a && b)
console.log(a || b)
```

If a variable isn't assigned a data type then it's either `null` or `undefined`. Undefined means that a variable hasn't been assigned a data type yet while null means that the variable won't be assigned any value.

```jsx
let a = undefined //This variable's value has not yet been defined.
let b = null //This variable does not have any data type.
```

> [!NOTE]
> The `typeof` keyword returns undefined when used against an undefined variable and returns an object when used against a null variable.
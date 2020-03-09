# JavaScript Fundamentals

The language of the web, JavaScript is a programming language used for a variety of purposes. Let's learn a little about it.

## History of JavaScript

JavaScript was invented in 1999 by Brendan Eich for Netscape (now Mozilla) over the course of 10 days. Keep this fact in mind as we learn some of the quirks later!

### What is ES6 and why does everyone talk about it?

This is the version of the JavaScript language. "ES6" stands for "ECMAScript6". It's also referred to as ES2015, which is the year that standard came out. ECMA is the European Computer Manufacturers Association, and it's based in Geneva. You don't really need to know that in order to use JavaScript, but it is a fun fact. What you do need to know is that going from ES5 to ES6 in 2015 was an enormous paradigm shift that introduced many new features and practices into the language.

> Note: If you ever hear your instructor talk about an "old way" of doing something in JavaScript, it's probably in reference to ES5 and before.

New versions of the language continue to come out every year. We're on ES10 as of the beginning of this class, but we should be getting ES11 right around when it wraps up. We don't really need to worry about this too much because all versions since ES6 have been relatively minor and mostly included additions rather than drastic changes.

> Note: You may hear the term "ES.Next". ES.Next is a dynamic name that refers to whatever the next version is at the time of writing. We might use it in class to describe upcoming features. Check out more on the [Wikipedia page](https://en.wikipedia.org/wiki/ECMAScript#History) if you are curious!

## What is a REPL?

REPL stands for Read-Evaluate-Print-Loop. Basically it's an interactive environment where you can run code. You may have used websites like [codepen](https://codepen.io/) or [repl.it](https://repl.it/) over the course of the pre-work. If you have discovered the developer tools in Chrome or Firefox, then you may have used the console tab for the same purpose. The most common usage for REPLs is when you don't want to take the time to make a file and just want to see how a bit of code runs quickly or to practice new concepts when learning code. 

For any exercises below, let's use [repl.it](https://repl.it/). 

#### 1. Take a minute to get signed in

Or, sign up if you don't have an account already. It's free!

#### 2. At the top right corner, you should see a button that says "new repl". 

![](https://res.cloudinary.com/briezh/image/upload/v1583773053/Screen_Shot_2020-03-09_at_9.56.56_AM_sa7pu9.png)

#### 3. Click that "new repl" button 

A menu that looks like this will come up:

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_305/v1583773147/Screen_Shot_2020-03-09_at_9.58.46_AM_irzf1z.png)

#### 4. Start typing "JavaScript". When it comes up, click on it

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_296/v1583774044/Screen_Shot_2020-03-09_at_10.13.37_AM_tow1hi.png)

#### 5. Name your repl "practice" and then click the green "create repl" button

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_400/v1583774223/Screen_Shot_2020-03-09_at_10.16.41_AM_x8sch7.png)

#### 6. Finally you have your repl ready to go!

You can type JavaScript code on the left side, and then run it with the green button at the top. The results of your code will display on the right.

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_757/v1583774402/Screen_Shot_2020-03-09_at_10.19.37_AM_kbd5ii.png)

## Comments

Comments are non-excuted code. Appropriate uses of comments include:

* Explanations for particularly tricky parts of code
* Definitions of functions or classes
* To temporarily disable one or more lines of code

> Tip: The most common inappropriate use of comments is to "save" old code. Remember this is what Git is for!

Comments come in two forms

### Single-line comments

```js
// descriptive stuff
```
### Multi-line comments

```js
/*
  These
  are
  comments on
  many lines
*/

```

## Primitive Types

There are 5 primitive types in JavaScript:

* Numbers
* Strings
* Booleans
* Null and Undefined (related but different concepts!)

### Numbers

Numbers are one of the *types* of **values** we want to be able to interact and play with in JS.

**Integers**

```
 ..., -1, 0, 2, 3, 4, 5, ...
```

**Floats (or Decimal numbers)**

```
 2.718, 3.14, .5, .25, etc
```

In JS these are both the same **type** of object, which it calls *Numbers*.

**Numbers Mini-Quiz**

Part 1: Type the following into your console or repl:

```js
2 + 2 * 3
```

What value do you get?
How would you get the `2 + 2` to execute before the `* 3`? (In other words, how would you change this expression to get 12?)

<details>
  <summary>Ready for the answers to part 1?</summary>
  <br />
  Just like in math, parentheses can be used to provide guidance for order of operations. We sincerely hope we aren't dredging up weird junior high memories by invoking the name PEMDAS (or Please Excuse My Dear Aunt Sally), which tell you among other things that items within parentheses are evaluated before other operators.
  <br /><br />
  So, in summary, we can get the result 12 by doing the following: `(2 + 2) * 3`. Try it out!
</details>

Part 2: Next, type the following into your console or repl:

```js
0.1 * 0.2 
```

What value do you get? 
What do you think is the cause of this problem?

<details>
  <summary>Ready for the answers to part 2?</summary>
  <br />
  0.1 * 0.2 = 0.020000000000000004
  <br /><br />
  You may be wondering what's going on. It turns out that this is caused by a floating point rounding error. While the vast majority of programming languages would simply round it off and clean this up for you, JavaScript just leaves you to have fun with this weird quirk.
  <br /><br />
  Just in case you ever do have to deal with this issue, read this Stack Overflow article about [how to deal with floating point precision in JavaScript](http://stackoverflow.com/questions/1458633/how-to-deal-with-floating-point-number-precision-in-javascript)
</details>

### Strings

Strings are collections of letters and symbols known as **Characters**, and we use them to deal with words and text in Javascript. Strings are just another type of **value** in Javascript.

```js
"John"
'Jane'
```

**Strings Exercise**

You can use operators on strings too! Try typing `"John" + "Jane"`. This is called String concatenation

### Tangent: Type coercion

Try this...

```js
"1" + 1
```

1. You probably expected the value 2 or perhaps an error. What did you get instead?
1. Without removing the quotes, how would you get this to equal 2? (**HINT**: Google "JavaScript Type Coersion")
1. Is the statement `1 + "1"` an equivalent statement to above (meaning, it gets the same result)?

### Booleans

Booleans are sometimes called "flags". They have only two values - `true` and `false` (or you can think of them as `on` and `off`!).

```js
true
false
```

### Null and Undefined

We'll get further into these later, but basically these values are used when there is no value. If you access something that doesn't have a value, you'll get `undefined`. If you purposely want a value to not exist, you might use the `null` value. 

> Fun Fact: Most languages don't make any distinction between these two concepts!

If you want a little more detail as to why these are two separate concepts, check out [this codeburst article](https://codeburst.io/javascript-whats-the-difference-between-null-undefined-37793b5bfce6) for a good high-level explanation with some code examples.

## Declaring Variables

You can think of a variable as a box that you can put something in. Consider the following line:

```js
var x = 5
```

What is happening? You've *declared* a variable named "x". It represents a memory space somewhere in your computer - additionally, in the same line, we've decided to fill up that memory space with the value 5. We are free to reassign this value later on. For example:

```js
// Here x is 5
var x = 5

// Now x will be 8
x = 8
```

> Note that during reassignment we do NOT use the var keyword again. Think of "var" as creating a new box, whereas reassignment is simply putting a new item in an existing box.

We can also declare a variable without providing a value. Think of this as obtaining a box that you might put something into later. For example, if we wanted to declare a variable called "y", but didn't yet have a value for it, it might look like this:

```js
var y
```

### Let vs Var vs Const??

You may have already encountered multiple ways of declaring variables. So which one should you use? Let's discuss each one individually to get an idea when and why they are used.

**const**

"Const" is short for "constant". This means that the value, once assigned, should not change. So, if we initially assigned a `const` variable a value like 5, it shouldn't change later on.

```js
const x = 5
```

We expect x to always be 5. In fact, we expect there to be an error if we try to reassign the value. Try running the following code in your repl:

```js
const x = 5
x = 8
```

What happens?

**let and var**

"Let" and "var" serve the same purpose in the majority of cases. "Let" is more specifically scoped, which doesn't really come into play until we start using for loops. "Var" was solely used previous to the ES6 version of the language. You can use either of them for now, we'll come back to this difference later.

## Printing

Printing just means showing text or data to the screen. 

> Note: For your repl or your developer tools console, it's interactive and automatically prints the last statement's result. When we run a local file with `node` on our terminal, we don't get this explicit evaluation.

We can explicitly tell our code we would like to print by using the `console.log()` function. This is a built-in feature of JavaScript. We can print the text "I love cats!" by running the following code:

```js
console.log("I love cats!")
```

We can also print the value of variables. This code will give the same result as above:


```js
let message = "I love cats!"
console.log(message)
```

**Mini-Activity**

PART 1: Run the following code in your repl:

```js
let message = "I love cats!"
console.log(message, message, message)
```

What prints out?
What is the separator character used between each print out of the message?

PART 2: Now, run this slightly altered code in your repl:

```js
let message = "I love cats!"
console.log(message + message + message)
```

What prints out?
What is the separator character used between each print out of the message?
What do you think is the difference between the two approaches?

<details>
  <summary>Answers for Mini-Activity</summary>
  <br /><br />
  You may have noticed that the code in part 1 was separated by commas. This feeds in three separate arguments. When we feed in several arguments, console.log separates them with a space.
  <br /><br />
  In part 2, the code was joined together with the `+` operator. The plus operator, when used on string types performs an action called "concatenation", which is the fancy term for smashing them all together. This concatenation operation happens before the print out happens. The code `console.log(message + message + message)` becomes `console.log("I love cats!I love cats!I love cats!")` before the console.log happens.
</details>

### String Concatenation vs String Interpolation

So, we learned a little bit about concatenation in the last activity. We can concatenate together whole sentences including variables and punctuation. Take this code for example:

```js
let name = "Brandi"
let title = "Instructor"
let class = "SEI"
console.log("Hello " + class + ", my name is " + name + ", and I will be your " + class + " " + title + "!")
// Prints: "Hello SEI, my name is Brandi, and I will be your SEI Instructor!"
```

It totally works... but it was a little tedious right? Let's try this instead:

```js
let name = "Brandi"
let title = "Instructor"
let class = "SEI"
console.log(`Hello ${class}, my name is ${name}, and I will be your ${class} ${title}!`)
// Prints: "Hello SEI, my name is Brandi, and I will be your SEI Instructor!"
```

Does it work for you? Notice that our normal quotes `'` or `"`, we instead have backticks, and we specify which parts are variables as opposed to literal text by using a dollar sign and then surrounding the variable's name with curly braces, like this: `${variableName}`.

**Mini-Activity**

Copy the following code into your repl:

```js
let name = "YOURNAMEHERE"
let title = "Student"
let class = "SEI"
console.log(`YOURTEXTHERE`)
// Prints: "Hello SEI, my name is YOURNAMEHERE, and I will be your SEI Student!"
```

Change "YOURNAMEHERE" to your own first name. Then, change "YOURTEXTHERE" such that it prints out "Hello SEI, my name is YOURNAMEHERE, and I will be your SEI Student!" using string interpolation (the backticks) and the variables `name`, `class`, and `title`.

## Operators

In addition to variables, we also have operators we can use to perform actions on those variables. We've already alluded to it above when we talked about PEMDAS and when we did string concatenation.

### Mathematical Operators

The available operators for numbers are:

| Operator | Purpose |
| ------- | ---------------------------- |
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulo |

What does the modulo operator do? 

### Comparison Operators

Comparison operators evaluate to booleans. Either the condition is met (`true`) or it isn't (`false`).

| Operator | Purpose |
| ------- | ---------------------------- |
| `==` | Equality |
| `===` | Type Strict Equality |
| `!=` | Inequality |
| `!==` | Type Strict Inequality |
| `<` | Less than |
| `<=` | Less than or equal to |
| `>` | Greater than |
| `>=` | Greater than or equal to |

**Mini-Activity**

You can plug in values to notice that each of these operators evaluates to a boolean. For example, in your repl or console, type the following:

```js
5 == 5
```

> Note: You can use `console.log(5 == 5)` to see the result if you aren't typing line by line into a console.

We know that 5 is equal to 5, and JavaScript knows it too, so it prints "true". Go ahead and try the following as well. What does each line evaluate to?:

```js
3 < 2
3 > 2
5 > 5
5 >= 5
"4" == 4
"4" === 4
4 === 4
```

Let's discuss - what's going on with those last three lines?

### Math Object

For more complex math operations, such as calculating an exponent, generating a random number, rounding a decimal, or using a constant like Pi, we can use JavaScript's built-in `Math` object. Let's look at some example code:

**Exponents**

```js
let twoToTheFourthPower = Math.pow(2, 4)
```

> Note: As of ES7, we also have access to the `**` operator for [exponents](https://2ality.com/2016/02/exponentiation-operator.html). Neat!

**Random Numbers**

JavaScript can generate a pseudo-random number for us with `Math.random()`. Go ahead and run the following code several times:

```js
console.log(Math.random())
```

You should get a different number every time, however you may notice that it is only generating decimals between 0 and 1. This is by design! If you would like to make a number in a certain range, you can multiply by that number. For example, if I want a range of 10 numbers:

```js
console.log(Math.random() * 10)
```

This will generate random values between 0.00000 and 9.99999. This probably still isn't what we want. Instead, we can also use the Math object to get to a whole number.

**Rounding, Floor, and Ceiling**

```js
let value = Math.random() * 10
Math.floor(value) // Go to nearest whole number lower than the decimal
Math.ceil(value) // Go to nearest whole number higher than the decimal
Math.round(value) // Go to nearest whole number lower or higher than the decimal, whichever is closest
```

For example, let's say I generated a random value of `8.121381319092333`.

```js
Math.floor(8.121381319092333) // Evaluates to 8
Math.ceil(8.121381319092333) // Evaluates to 9
Math.round(8.121381319092333) // Evaluates to 8
```

In our case, we probably want the lowest value to be 1 and the highest number to be 10. Thus, for a range of 0.000000 to 9.99999, we likely want to use `Math.ceil()`

**Accessing Pi**

PI is a constant on the math object. You can use it just like this:

```js
console.log(Math.PI)
```

In a calculation, such as the circumference of a circle, `C = 2πr`, we can use the PI constant to calculate the result. Let's say we want to know what the circumference of a medium pizza is. A typical medium pizza is 12 inches across.

```js
// We know the pizza is 12 inches in diameter
let diameter = 12

// The radius is half of the diameter
let radius = diameter / 2

// Now we can use the equation C = 2πr
let circumference = 2 * Math.PI * radius

// Print out the raw value
console.log('A medium pizza has', circumference, 'inches of crust!')

// Let's round it to the nearest whole number
console.log('A medium pizza has roughly', Math.round(circumference), 'inches of crust!')
```

You should get a result like this:

![](https://res.cloudinary.com/briezh/image/upload/c_scale,w_615/v1583781557/Screen_Shot_2020-03-09_at_12.18.57_PM_yrsdtb.png)

**Mini-Activity**

You may recall that the area of a circle is calculated with πr<super>2</super>. Let's find out what the difference in area is between a medium pizza and a large pizza. A medium pizza as noted above has a diameter of 12 inches. A large pizza has a diameter of 14 inches. Let's use this starter code:

```js
let mediumDiameter = 12
let largeDiameter = 14

// 1. Calculate radius of both
let mediumRadius = ???
let largeRadius = ???

// 2. Use the Math.pow or ** operator to find the square of each pizza size's radius
let mediumRadiusSquared = ???
let largeRadiusSquared = ???

// 3. Use the equation to perform the calculation A = πr^2 for each pizza size
let mediumArea = ???
let largeArea = ???

// 4. Print each out using console.log

// 5. Console.log the difference between a large and medium in square inches
```

## Complex Types: Arrays and Objects

TODO

## Built-in String Methods

TODO

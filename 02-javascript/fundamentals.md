# JavaScript Fundamentals

The language of the web, JavaScript is a programming language used for a variety of purposes. Let's learn a little about it.

## History of JavaScript

JavaScript was invented in 1999 by Brendan Eich for Netscape (now Mozilla) over the course of 10 days. Keep this fact in mind as we learn some of the quirks later!

### What is ES6 and why does everyone talk about it?

This is the version of the JavaScript language. "ES6" stands for "ECMAScript6". It's also referred to as ES2015, which is the year that standard came out. ECMA is the European Computer Manufacturers Association, and it's based in Geneva. You don't really need to know that in order to use JavaScript, but it is a fun fact. What you do need to know is that going from ES5 to ES6 in 2015 was an enormous paradigm shift that introduced many new features and practices into the language.

> Note: If you ever hear your instructor talk about an "old way" of doing something in JavaScript, it's probably in reference to ES5 and before.

New versions of the language continue to come out every year. We're on ES10 as of the beginning of this class, but we should be getting ES11 right around when it wraps up. We don't really need to worry about this too much because all versions since ES6 have been relatively minor and mostly included additions rather than drastic changes.

> Note: You may hear the term "ES.Next". ES.Next is a dynamic name that refers to whatever the next version is at the time of writing. We might use it in class to describe upcoming features.

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

"Let" and "var" serve the same purpose in the majority of cases. "Let" is more specifically scoped, which doesn't really come into play until we start using for loops. "Var" was solely used previous to the ES6 version of the language.

## Printing

TODO

## Operators

TODO

## Complex Types: Arrays and Objects

TODO

## Built-in String Methods

TODO

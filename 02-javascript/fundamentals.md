# JavaScript Fundamentals

The language of the web, JavaScript is a programming language used for a variety of purposes. Let's learn a little about it.

## History of JavaScript

JavaScript was invented in 1999 by Brendan Eich for Netscape (now Mozilla) over the course of 10 days. Keep this fact in mind as we learn some of the quirks later!

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
/**
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

This can infrequently cause problems!

```js
0.1 * 0.2 = 0.020000000000000004
```

[How to deal with floating point precision in JavaScript](http://stackoverflow.com/questions/1458633/how-to-deal-with-floating-point-number-precision-in-javascript)

**Numbers Exercise**

```js
2 + 2 * 3
```

How would you get the `2 + 2` to execute before the `* 3`? In other words, how would you change this expression to get 12?

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

1. Without removing the quotes, how would you get this to equal 2?
1. Is the statement `1 + "1"` an equivalent statement to above (meaning, it gets the same result)?

## Declaring Variables

TODO

## Printing

TODO

## Operators

TODO

## Complex Types: Arrays and Objects

TODO

## Built-in String Methods

TODO

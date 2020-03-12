# JavaScript Conditionals

JavaScript conditionals (if statements) are one way that we alter the control flow of our code. Sometimes we only want code to execute if a certain condition is met. For example, I want my smart thermostat to turn up the heat _only if I am cold_! Let's talk about control flow in a general sense for a second.

## Control Flow

Control flow is the order in which the computer executes statements in a script. Javascript executes top-to-bottom, _unless we alter the control flow_.

**Why/how would we alter the control flow?**

1. Skip lines of code based on a condition.
1. Repeat lines of code when traversing a data set or just for the sake of DRY code.

**Here are some statements we can use to alter the control flow:**

1. [if](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/if...else)
1. [switch](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/switch)
1. [while](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/while)
1. [for](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
1. [for...in](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in)

But before that, let's create the expressions needed for these statements

## Boolean Expressions

Before we can make an if statement, we need to make a boolean expression for it. Generally an if statement follows this format:

```js
if (BOOLEAN EXPRESSION) {
  // CODE THAT RUNS IF THE BOOLEAN EXPRESSION EVALUATED TO TRUE
}
```

### = vs == vs === 

#### = (Assignment)

The single equals sign is for assignment. If you've used this inside of an if statement it is _almost certainly a mistake_!

Unfortunately, the result of assignment evaluates to a truthy value, so this will create some weird, unexpected behavior. For example, let's say you meant to write this code with two equals signs:

```js
let x = 4
if (x == 5) {
  // This appropriately doesn't execute
  console.log('This should not be printed')
}
```

But instead, you forgot one of the equals signs and wrote this instead:

```js
let x = 4
if (x = 5) {
  // AWW CRAP
  console.log('This should not be printed')
}
```

> Fun fact: Once we get to Python, it will helpfully and appropriately throw an error when you make a typo like this. However, until that time, we're using JavaScript, so let's learn to love jank for now!

#### == (Equality)

The double equals represents a loosey-goosey kind of equality. To see what we mean by this, let's do a short partner activity.

**Step 1: Get into pairs or small table groups (max 3 people)**

**Step 2: For each of the following expressions, guess whether you'll get false or true or something else as a result**

```js
5 == 5

5 == "5"

true == true

true == "true"

false == ""

0 == ""

"Hello" == "World"
```

**Step 3: Try running the above expressions on your browser console**

**Step 4: Talk about it**

What did you expect? Was that what happened?

#### === (Type Strict Equality)

You likely have a good idea where this is going! Let's use the triple equals now.

**Step 1: Get into the same groups from the previous activity**

**Step 2: For each of the following expressions, guess whether you'll get false or true or something else as a result**

```js
5 === 5

5 === "5"

true === true

true === "true"

false === ""

0 === ""

"Hello" === "World"
```

**Step 3: Try running the above expressions on your browser console**

**Step 4: Talk about it**

What did you expect? Was that what happened? What do you conclude is the difference between double and triple equals?

### If/Else Statements

If statements are formed like this:

```js
let age = 7
if (age == 5) {
  console.log('Enter kindergarten')
}
```

The code inside of the if statement only runs if the condition is met. Otherwise this code is skipped entirely! This is pretty easy to understand, but we'll get more complicated pretty quick. Let's talk about `else` and `else if` statements. `else` and `else if` statements must be attached to an `if`. They can't just wander around by themselves.

#### Else If (Additional condition)

The `else if` statement is meant to provide an additional condition. You can have any number of them. Let's add a couple to our previous example. We'll enroll our child in the nearby elementary school:

```js
let age = 2
if (age == 5) {
  console.log('Enter kindergarten')
}
else if (age == 6) {
  console.log('Enter 1st Grade')
}
else if (age == 7) {
  console.log('Enter 2nd Grade')
}
else if (age == 8) {
  console.log('Enter 3rd Grade')
}
else if (age == 9) {
  console.log('Enter 4th Grade')
}
else if (age == 10) {
  console.log('Enter 5th Grade')
}
else if (age < 5) {
  console.log('Are you sure you are ready for school?')
}
```

> My kid Jace is 2. He isn't quite ready for school!

#### Else (The catch-all)

### Logical Operators

You may have come across logical operators `&&` (and) and `||` (or). These are used to join multiple boolean expressions together.

```js
let bored = true
let hungry = false

if (hungry || bored) {
  console.log('Open fridge')
}
```

In the above example, only one or the other of `bored` and `hungry` must be true. It's fine if they're both true. The only way we get to skip this if statement is if both `hungry` and `bored` are `false`. You can change the values of `bored` and `hungry` to verify this. 

The logical and operator, `&&`, only evaluates to true if both sides are `true`. Consider this code:

```
let paidCoverCharge = true
let age = 18

if (age >= 21 && paidCoverChange) {
  console.log('Enter the club')
}
```

Change the values of `age` and `paidCoverCharge` in order to see how `&&` works.

### Truthiness

If you recall, back in the JS fundamentals lesson, we mentioned the idea of "truthiness" and "falsiness". This is a way we can essentially create a shorthand boolean expression. It works like this: Each value in JavaScript has an inherent _truthy_ or _falsy_ value when used as a boolean expression. Consider the following code:

```js
let x = 5
if (x) {
  console.log('x is truthy!')
}
else {
  console.log('x is falsy!'
}
```

Try running it. What prints out? What value of x results in truthy? What value of x results in falsy?

#### Falsy Values

As you may have noticed above, values are generally truthy unless otherwise specified. It's easiest to just memorize the falsy values and assume everything else is truthy. Each primitive type has a falsy value, and there is an additional falsy value known as `NaN` - not a number.

| Falsy Value | Notes |
| -------- | ----------------- |
| `""` | Empty string (String type) |
| `0` | zero (Number type) |
| `false` | false (Boolean type) |
| `null` | null (Null type) |
| `undefined` | undefined (Undefined type) |
| `NaN` | Not a Number |

> Warning: Complex types such as arrays and objects are based on memory addresses and therefore are ALWAYS truthy. You may have expected an empty array `[]` or an empty object `{}` to be falsy, and no one would blame you for thinking that, but alas, JavaScript is janky.

Learn more about JavaScript's 6 falsy values on [this freecodecamp article](https://guide.freecodecamp.org/javascript/falsy-values/).

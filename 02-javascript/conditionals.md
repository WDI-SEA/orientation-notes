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

### = vs == vs === 

TODO

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


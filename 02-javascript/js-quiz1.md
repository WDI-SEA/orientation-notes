# JavaScript Fundamentals

## Your Name: ______________________ Your Score: ___________________

#### 1) In JavaScript, how can I declare a variable? (Circle ALL correct answers - there may be more than one! 8 points)

* `x = 5`
* `let x = 5`
* `5 = x`
* `const x = 5`
* `var 5 = x();`
* `var(...args);`
* `var x = 5;`
* `var = x;`

#### 2) What does `===` do that `==` doesn't? (1 point)

* a) Checks for equality (instead of assignment)
* b) Checks for a deep copy of an array
* c) Checks that the types being compared match (as well as value)
* d) Assigns a boolean value type when appropriately matched to the incoming data
* e) None of the above

#### 3) What does `==` do that `=` doesn't? (1 point)

* a) Checks for equality (instead of assignment)
* b) Checks for a deep copy of an array
* c) Checks that the types being compared match (as well as value)
* d) Assigns a boolean value type when appropriately matched to the incoming data
* e) None of the above

#### 4) An `else` can live independently from an `if` statement. True or False? (1 point)

* a) True
* b) False
* c) All of the Above 

**Consider the following code, then answer questions 5 and 6**

```js
let numPeople = 2;
if (numPeople == 1) {
  console.log('Hello future student!');
}
else if (numPeople == 2) {
  console.log('Hello to both of you future students!');
}
else if (numPeople > 0) {
  console.log('Hello SEI class!');
}
```

#### 5) An `if` statement includes a conditional piece. In the code above, this condition is `numPeople == 1`. This conditional: (1 point)

* a) Evaluates to a boolean
* b) Evaluates to an integer
* c) Evaluates to an array
* d) Doesn't evaluate because we need `===` instead of `==`
* e) Doesn't evaluate because we need `=` instead of `==`

#### 6) In the above code, what prints out? (1 point)

* a) 'Hello future student!'
* b) 'Hello to both of you future students!'
* c) 'Hello SEI class!'
* d) Both b and c
* e) None of the Above

#### 7) The `!` operator (sometimes called a "bang") is used for: (1 point)

* a) Negation (i.e., Not)
* b) Inversion (i.e., Absolute Value)
* c) Factorials (Like in mathematics)
* d) Aggregation (of statistics, such as mean, standard deviation, etc)
* e) Interpolation (i.e., to queue the injection points for the arguments)

#### 8) The line `i++` does what? (2 points)

* a) Adds one to the number `i`
* a) Is equivalent to `i = i + 1`
* a) Is equivalent to `i += 1`
* a) All of the Above
* e) None of the Above

#### 9) What does a multi-line comment (A comment that spans multiple lines) look like in JavaScript? (1 point)

* a) `<!-- This -->`
* b) `<% This %>`
* c) `{{ This }}`
* d) `# This #`
* e) `/* Or This */`

# Lab: Loops

Take a look at the array below. Use the pseudocode you wrote in the previous lab to find the largest number and log it to the console in the following format: `"The highest number is #"`. Now that we know how to use if statements and loops, we should be able to implement the solution we wrote from that pseudocode!

```js
var numbers = [20, 3, 5, 7, 13, 30];
```

If you need a hint on how to solve this one, take a look at the steps listed below, along with the linked resources. 

Steps:
- First create a variable `highestNumber` and give it a value of the number `0`.

- Then use a [`for` loop](https://www.w3schools.com/js/js_loop_for.asp) to loop through the `numbers` array. 
	- 	Your `for` loop should look something like this:

		```js
		for (let i = 0; i < numbers.length; i++) {
		  // YOUR CODE HERE!
		}
		```
- Within the loop, use an [`if` statement](https://www.w3schools.com/js/js_if_else.asp) to see if the current number (`numbers[i]`) is greater than the number that is currently stored in `highestNumber`.
- If so, save `numbers[i]` in the `highestNumber` variable.
	- Hint: You only need to use `var` when you initially set up a variable. To update a variable, simply use the variable name (`highestNumber`) followed by `=` followed by the new value (`numbers[i]`).
- On the line after the `for` loop, log `highestNumber` to the console in this format: "The highest number is #"`.

## Bonus

Can you add in the smallest number as well? How does your code change if you find both the largest and smallest numbers? Write some code that prints out the following: 

`"The highest number is #, and the smallest number is #"`

> Try using the backticks for string interpolation!

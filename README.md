# JavaScript Closure Problem with setTimeout

This repository demonstrates a common JavaScript closure issue that arises when using `setTimeout` within a loop.  The problem stems from how closures capture variables.

## The Bug
The `bug.js` file contains a function `myFunction` that uses a `for` loop and `setTimeout` to log the value of `i` after a delay.  Due to how closures work in JavaScript, all the callbacks will log the final value of `i` (which is 10) instead of the value of `i` at the time the `setTimeout` was called.

## The Solution
The `bugSolution.js` file shows the solution to this problem. It uses an immediately invoked function expression (IIFE) to create a new scope for the variable `i`, effectively capturing its value correctly within each setTimeout callback.

## How to Run
1. Clone this repository.
2. Open both `bug.js` and `bugSolution.js` files in your browser's developer console or a JavaScript environment.
3. Execute the code and observe the differences in output.
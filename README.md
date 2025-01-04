# JavaScript Closure Issue in setTimeout Loop

This repository demonstrates a common issue in JavaScript involving closures and the `setTimeout` function within a loop.

The problem arises because the `setTimeout` callback function does not capture the value of `i` at the time of its creation. Instead, it captures a reference to the variable `i`, which changes during the loop execution.  This results in all callbacks logging the final value of `i`, which is 10.

The solution involves using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, thus capturing the correct value of `i` for each callback.
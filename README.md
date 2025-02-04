# Unexpected String Truncation in Recursive PHP Function

This repository demonstrates a bug in a PHP recursive function that unexpectedly truncates strings within deeply nested arrays. The function `processData` aims to process an array, truncating strings longer than 10 characters. However, it exhibits unexpected behavior when dealing with nested structures. 

## Bug Description

The core issue lies in how the function handles string length checks within nested arrays.  When a string exceeds 10 characters, it's correctly truncated at the top level.  However, if that long string is nested within an array, it causes problems.  The function should truncate the string no matter its nesting level. This also requires handling null values and empty arrays to avoid unexpected errors.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php`.
3. Observe the unexpected output, where truncation may not occur as expected in nested arrays.

## Solution

The `bugSolution.php` file provides a corrected version of the `processData` function, resolving the truncation issue and handling edge cases robustly. It uses more robust checks and recursive function calls to handle different array structures properly.
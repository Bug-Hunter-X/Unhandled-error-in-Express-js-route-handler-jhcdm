# Express.js Unhandled Error
This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  The `bug.js` file shows the problematic code, which fails to handle cases where the user ID is not found or is not a valid integer. The `bugSolution.js` file provides a corrected version with robust error handling. 

## Problem
The original code directly attempts to parse the user ID as an integer and access the user object, without checking if the ID is valid or if the user exists. This can lead to unexpected crashes or errors in production. 

## Solution
The solution involves explicit checks for valid input: 
1. **Type checking:**  Verifying the userId is a number.
2. **Existence check:** Ensuring the user exists in the users array. 
3. **Error handling:** Returning appropriate HTTP status codes and error messages for invalid input. 
# Express.js Route Handler Error Handling Bug

This repository demonstrates a common bug in Express.js route handlers:  missing error handling for invalid input.  The `bug.js` file contains code that is vulnerable to errors if an invalid user ID is provided.  The `bugSolution.js` file shows how to properly handle these errors to prevent unexpected behavior.

## Bug Description

The `bug.js` code attempts to retrieve a user based on their ID, parsed from the request parameters.  However, it lacks error handling for cases where the `userId` is not a valid integer. This can lead to runtime errors or unexpected behavior.

## Solution

The `bugSolution.js` file shows how to address this bug by adding error handling. The code checks if `parseInt(userId)` returns `NaN` before proceeding with the user lookup and uses proper status codes to provide a helpful response to the client.
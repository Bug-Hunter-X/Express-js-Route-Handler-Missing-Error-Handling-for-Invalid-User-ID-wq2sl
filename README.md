# Express.js Route Handler Error Handling Bug

This repository demonstrates a common error in Express.js route handlers:  lack of error handling for invalid input.  Specifically, the provided code attempts to access a user by ID, but doesn't handle the scenario where the ID is not a valid number, causing a runtime error.

## Bug Description

The `bug.js` file contains an Express.js route that retrieves a user based on their ID.  However, it fails to handle the case where the `id` parameter is not a valid integer, leading to potential errors if a non-numeric ID is passed.

## Solution

The `bugSolution.js` file provides a corrected version that includes robust error handling.  It checks whether the `id` parameter is a valid integer and handles the case where the user is not found.

## How to reproduce the bug

1.  Clone the repository.
2.  Run `npm install express` to install dependencies.
3.  Run `node bug.js`. 
4.  Send a request to `/users/abc` (or any non-numeric ID). You'll see an error in your console.

## How to see the solution

1.  Run `node bugSolution.js`.
2. Send the same request to `/users/abc`. You'll see a 'User not found' response with status code 404.
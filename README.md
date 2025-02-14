# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the example shows a route that fetches a user by ID but fails to handle cases where the ID is not a valid integer.

## Bug

The `bug.js` file contains an Express.js route handler that attempts to fetch a user from an array based on the ID passed in the request parameters.  However, it doesn't handle potential errors if the ID is not a number, leading to potential crashes or unexpected behavior.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler.  It includes explicit checks to ensure the ID is a number before attempting to parse it.  If the ID is invalid, it returns a proper HTTP error response.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` (for the buggy version) and then `node bugSolution.js` (for the fixed version).
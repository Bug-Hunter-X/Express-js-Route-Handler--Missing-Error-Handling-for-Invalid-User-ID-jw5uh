# Express.js Route Handler: Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without validation, which can lead to unexpected errors.

## Bug

The provided `bug.js` file contains the faulty code.  It fails to handle cases where the `userId` is not a valid integer, resulting in potential crashes or unexpected behavior.

## Solution

The `bugSolution.js` file demonstrates the corrected code.  It includes robust error handling to check if `userId` is a valid number before attempting to access the user data.  Appropriate HTTP status codes are also used to communicate errors gracefully to the client.
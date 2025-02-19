# MongoDB $inc operator error
This repository demonstrates a common error when using the `$inc` operator in MongoDB. The `$inc` operator is designed to increment numeric fields only.  Attempting to use it with a non-numeric field leads to an error. The `bug.js` file contains the erroneous code, while `bugSolution.js` shows the correct implementation.

**Error:**
The error that will occur is related to the type mismatch in the field being incremented using the `$inc` operator.  The specific error message might vary slightly depending on the MongoDB driver used, but it will generally indicate that the operation failed because the field is not a number.

**Solution:**
Ensure that the field you're using with `$inc` is of a numeric type (int, double, etc.). If you need to update a string field, use the `$set` operator instead.
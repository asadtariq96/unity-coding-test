## Unity Coding Test - Asad Tariq


## Answer #1

 
 - The HTTP method should be used to describe the verb or action being performed and the endpoint should remain the same, so the requests should be `POST /users`, `DELETE /users/:id`, `PUT /users/:id`
 - For updating user resource, a single `PUT /users/:id` should be used instead of `POST /users/:id/update`
 - `/update`, `/rename`, `/update-timezone` are redundant and not required, therefore a more suitable approach would be `PUT /users/:id` or `PATCH /users/:id` depending on whether the whole user resource needs to be updated or only few parts of it such as `name` and `timezone`
 - If username already exists, HTTP status code should be `409` instead of `200`

## Answer #2

- `sumB` is more performant because of manual loop unrolling, but does not check if `*a` is multiple of `4` or not, which can cause errors in result.
- `sumA` is more typesafe because of `a[SIZE][SIZE]` , but is less performant due to column-order traversal which will result in a lot of cache misses (but it can be fixed by changing the order of the loops).
- I will prefer `sumA` because its more readable and does not require refactoring of the function itself if the array size changes as long as the 2D array is equal rows and columns

## Answer #3
- The whole function violates one of the most important cryptography principles, i.e., never write your own crypto, and the user should use built-in functionality provided by the programming language.
- Using same salt for all passwords instead of generating unique salt for each password.
- Using a unsuitable hash function `MD5` because its very fast, allowing very fast brute force attacks.

## Answer #4
- `const deposits = user.transactions.history.deposits` assumes that `deposits` exist in that user's transactions' history, so there should be some checks / exception handling in place.
- `var i` should be replaced by `let i`.
- For type safety, it would be better to cast `deposits.amount` to `Number`

## Answer #5
- `db.game_accounts.findOne` might not find a valid account which fulfils the criteria, so there should be a check in place like this: `if (fromAccount)` and `if (toAccount)`
- Both `update` queries should be wrapped in a transaction to make the debit and credit operation atomic, or the query shall be written in such a way that only 1 write operation takes place.
## Answer #6
- To increase readability of the code, it would be better to change the `if (!isCredit)` to `if (isCredit)` and then perform the credit operation in `if` block and the debit operation in the `else` block
- The function `increaseBalance` may be broken down into 2 separate functions `debit` and `credit` which perform only 1 task, to better adhere to single-responsibility principle.
## Answer #7
- Indexing
- Query optimization
- Sharding
- Read replicas
## Answer #8
https://jsfiddle.net/n85pwxyc/
## Answer #9
https://jsfiddle.net/eh9c1jbL/2/

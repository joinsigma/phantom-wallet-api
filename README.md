# Slap 'n Go API
Your perfect playground to practice CRUD operations in a safe, simulated e-wallet environment without the risk of real currency.

##  DELETE /deleteUser/:username
Delete a specific user identified by the `username` parameter.

#### HTTP DELETE Request
```
https://e-wallet-api-server.sigma-schoolsc1.repl.co/users/:username
```

<details>
 <summary> Parameters, Success and Error responses </summary>

  ### URL Parameters
 
  Parameter | Description
  --------- | -----------
  username  | The username of the user to be deleted.

  ### Success Response

  <details>
  <summary>Status 200</summary>

  Response content:

  ```json
  {
    "message": "User {username} has been deleted."
  }
  ```
  </details>

  ### Error Responses
  <details>
  <summary>Status 403</summary>
  Response content:

  ```json
  {
    "message": "Invalid API key."
  }
  ```
  </details>

  <details>
  <summary>Status 404</summary>
  Response content:

  ```json
  {
    "message": "User {username} not found."
  }
  ```
  </details>
  
</details>

## DELETE /deleteTransaction/:username

Delete a specific transaction for a user identified by the `username` parameter.

#### HTTP Delete Transaction Request
https://e-wallet-api-server.sigma-schoolsc1.repl.co/deleteTransaction/:username

#### Request Body
The request body must be a JSON object containing the `amount` property. For example:
```json
{
  "amount": 10
}
```

<details>
<summary>Parameters, Success and Error Responses</summary>
 
  ### URL Parameters
 
  Parameter | Description
  --------- | -----------
  username  | The username of the user to be deleted.
 
### Success Response
<details>
<summary>Status 200</summary>
Response content:
 
```json
{
  "message": "Transaction for user {username} has been deleted successfully!",
  "name": "{username}",
  "transactions": []
}
```
</details>
 
### Error Responses
<details>
<summary>Status 418</summary>
Response content:
 
 ```json
{
  "error": "Error Transaction Request: 'amount' is required in request body."
}
```
</details>
</details>

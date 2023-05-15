# phantom-wallet-api
Your perfect playground to practice CRUD operations in a safe, simulated e-wallet environment without the risk of real currency.

## DELETE /deleteUser/:username

Delete a specific user identified by the `username` parameter.

### HTTP DELETE Request
```
https://e-wallet-api-server.sigma-schoolsc1.repl.co/deleteUser/:username
```

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
  "message": "User deleted successfully."
}
```
</details>
  
### Error Responses
<details>
<summary>Status 400</summary>
Response content:
  
```json
{
  "message": "Invalid username."
}
```
</details>
  
<details>
<summary>Status 418</summary>
Response content:
  
```json
{
  "message": "Username not found."
}
```
</details>

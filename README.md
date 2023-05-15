# phantom-wallet-api
Your perfect playground to practice CRUD operations in a safe, simulated e-wallet environment without the risk of real currency.

## DELETE /deleteUser/:username

Delete a specific user identified by the `username` parameter.

### HTTP DELETE Request
```
https://e-wallet-api-server.sigma-schoolsc1.repl.co//users/:username
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
  "message": "'Invalid API key."
}
```
</details>
  
<details>
<summary>Status 404</summary>
Response content:
  
```json
{
  "message": "User ${username} not found."
}
```
</details>

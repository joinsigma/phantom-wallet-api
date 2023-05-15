# phantom-wallet-api
A simple simulated e-wallet environment to hone your skills without dealing with real currency. A perfect playground for students to learn, practice, and master their CRUD and API development skills.

## DELETE /deleteUser/:username

Delete a specific user identified by the `username` parameter.

### HTTP Request

DELETE https://<your-api-url>/deleteUser/:username

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
</details>
Error Responses
<details>
<summary>Status 400</summary>
Response content:

{
  "message": "Invalid username."
}
</details>
<details>
<summary>Status 418</summary>
Response content:

{
  "message": "Username not found."
}
</details>
```

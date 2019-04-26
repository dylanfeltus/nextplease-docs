# Authentication

> Example request

```shell
curl https://nextplease.io/api/v1/sessions \
  -H "Content-Type: application/json" \
  -d '{"email":"example@gmail.com","password":"password"}'
```

> Example response

```json
{
  "authentication_token":"4nxAn76-TumRoaexkDqV"
}
```

Next Please uses authentication tokens to allow access to the API.  

You send email and password for the user you are trying to authenticate and receive a token.

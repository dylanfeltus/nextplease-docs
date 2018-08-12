# Users

## Get all users

> Example request

```shell
curl https://nextplease.io/api/v1/users \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "email":"example@gmail.com",
    "name": "Example User",
    "username":"exampleuser",
    "role":"owner",
    "avatar":"http://s3.us-east-2.amazonaws.com/nextplease/../../",
    "created_at": "2018-08-08T18:46:03.081Z"
  }
]
```

This endpoint retrieves all users for an account.

### HTTP Request

`GET https://nextplease.io/api/v1/users`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the user.
email | string | The users email address.
name | string | The users name.
username | string | The username.
role | string | The users access level. Options include `owner`, `admin`, `engineer`, `product owner`, `member`
avatar | string | The users avatar if one exists.
created_at | datetime | When the user was added to the account.

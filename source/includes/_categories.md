# Categories

## Get all categories

> Example request

```shell
curl http://nextplease.test/api/v1/categories \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "name": "Example category",
    "description": "Description for example category",
    "created_at": "2018-08-08T18:46:03.081Z"
  }
]
```

This endpoint retrieves all categories for an account.

### HTTP Request

`GET http://nextplease.test/api/v1/categories`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the category.
name | string | This is the name of the category.
description | text | This is the description of the category.
created_at | datetime | When the category was created.

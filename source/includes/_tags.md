# Tags

## Get all tags

> Example request

```shell
curl https://nextplease.io/api/v1/tags \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "name": "Example tag"
  }
]
```

This endpoint retrieves all tags for an account.

### HTTP Request

`GET https://nextplease.io/api/v1/tags`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the tag.
name | string | This is the name of the tag.

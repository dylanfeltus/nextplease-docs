# Account info

## Get account info

> Example request

```shell
curl http://nextplease.test/api/v1/accounts \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "company_name":"ACME, Inc.",
    "brand_color":"DD3A92",
    "avatar":"http://s3.us-east-2.amazonaws.com/nextplease/../../",
    "logo":"http://s3.us-east-2.amazonaws.com/nextplease/../../",
    "created_at": "2018-08-08T18:46:03.081Z"
  }
]
```

This endpoint retrieves some information for the current account.

### HTTP Request

`GET http://nextplease.test/api/v1/accounts`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the account.
company_name | string | The company name for the account.
brand_color | string | The hex code brand color for the account.
avatar | string | The company avatar url if one exists.
logo | string | The company logo url if one exists.
created_at | datetime | When the accounts was created.

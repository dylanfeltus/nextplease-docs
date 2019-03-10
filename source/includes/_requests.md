# Requests

## Get all requests

> Example request

```shell
curl https://nextplease.io/api/v1/requests \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "title": "Example title",
    "content": "Description for example request",
    "category_id": 123,
    "public": true,
    "public_content": "This is the public description for example request",
    "created_at": "2018-08-08T18:46:03.081Z",
    "status": "open"
  }
]
```

This endpoint retrieves all requests.

### HTTP Request

`GET https://nextplease.io/api/v1/requests`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the request.
title | string | This is the title of the request.
content | text | This is the description of the request.
category_id | integer | The ID for the category this request belongs to.
public | boolean | This will be true if the request is publicly available. This is false by default.
public_content | text | This is the description that is shown on the public roadmap or changelog.
created_at | datetime | When the request was created.
status | string | The status for the request. This can be "open", "review", "planned", "pending", or "closed"

## Get a specific request

> Example request

```shell
curl "https://nextplease.io/api/v1/requests/<ID>"
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
{
  "id": 123,
  "title": "Example title",
  "content": "Description for example request",
  "category_id": 123,
  "public": true,
  "public_content": "This is the public description for example request",
  "created_at": "2018-08-08T18:46:03.081Z",
  "status": "open",
  "people": [
    {
      "id": 123,
      "name": "John Doe",
      "email": "john@doe.com",
      "user_id": 1,
      "created_at": "2018-08-12T01:36:12.893Z"
    },
    {
      "id": 124,
      "name": null,
      "email": "another@one.com",
      "user_id": 2,
      "created_at": "2018-08-12T01:41:35.759Z"
    }
  ],
  "comments": [
    {
      "id": 123,
      "content": "A comment!",
      "user_id": 1,
      "created_at": "2018-08-12T01:50:44.148Z"
    }
  ]
}
```

This endpoint retrieves a specific request along with all associated people and comments.

### HTTP Request

`GET https://nextplease.io/api/v1/requests/<ID>`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the request.
title | string | This is the title of the request.
content | text | This is the description of the request.
category_id | integer | The ID for the category this request belongs to.
public | boolean | This will be true if the request is publicly available. This is false by default.
public_content | text | This is the description that is shown on the public roadmap or changelog.
created_at | datetime | When the request was created.
status | string | The status for the request. This can be "open", "review", "planned", "pending", or "closed"

## Create a request

> Example request

```shell
curl https://nextplease.io/api/v1/requests \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"title":"Request title","content":"Description of the request.","category_id":1}'
```

> Example response

```json
{
  "message":"Successfully created request",
  "request":{
    "id":123,
    "title":"Example title",
    "content":"Description for example request",
    "category_id":123,
    "public":true,
    "public_content":"This is the public description for example request",
    "created_at":"2018-08-12T02:03:15.802Z",
    "status": "open",
  }
}
```

This endpoint will create a new request.

### HTTP Request

`POST https://nextplease.io/api/v1/requests`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
title | string | This is the title of the request.
content | text | This is the description of the request.
category_id | integer | The ID for the category this request belongs to.

## Update a request

> Example request

```shell
curl https://nextplease.io/api/v1/requests/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"title":"New request title"}' \
  -X PUT
```

> Example response

```json
{
  "message":"Successfully updated request",
  "request":{
    "id":123,
    "title":"New request title",
    "content":"Description for example request",
    "category_id":123,
    "public":true,
    "public_content":"This is the public description for example request",
    "created_at":"2018-08-12T02:03:15.802Z",
    "status": "open",
  }
}
```

This endpoint will update an existing request.

### HTTP Request

`PUT https://nextplease.io/api/v1/requests/<ID>`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
title | string | This is the title of the request.
content | text | This is the description of the request.
category_id | integer | The ID for the category this request belongs to.

## Delete a request

> Example request

```shell
curl https://nextplease.io/api/v1/requests/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -X DELETE
```

> Example response

```json
{
  "message":"Successfully deleted request"
}
```

This endpoint will delete a request.

### HTTP Request

`DELETE https://nextplease.io/api/v1/requests/<ID>`

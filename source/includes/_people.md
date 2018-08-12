# People

## Get all people

> Example request

```shell
curl http://nextplease.test/api/v1/people \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "name": "Example person",
    "email": "example@gmail.com",
    "created_at": "2018-08-08T18:46:03.081Z"
  }
]
```

This endpoint retrieves all people.

### HTTP Request

`GET http://nextplease.test/api/v1/people`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the person.
name | string | The name of the person.
email | string | The email of the person.
created_at | datetime | When the person was created.

## Get a specific person

> Example request

```shell
curl "http://nextplease.test/api/v1/people/<ID>"
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
{
  "id": 123,
  "name": "Example person",
  "email": "example@gmail.com",
  "created_at": "2018-08-08T18:46:03.081Z",
  "requests": [
    {
      "id": 123,
      "title": "Request title",
      "content": "Description of the request.",,
      "category_id": 1,
      "public": false,
      "public_content": null,
      "created_at": "2018-08-12T02:08:45.008Z",
      "archived_at": null
    }
  ]
}
```

This endpoint retrieves a specific person along with all associated requests.

### HTTP Request

`GET http://nextplease.test/api/v1/people/<ID>`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the person.
name | string | The name of the person.
email | string | The email of the person.
created_at | datetime | When the person was created.

## Create a person

> Example request

```shell
curl http://nextplease.test/api/v1/people \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"name":"Example person","email":"example@gmail.com"}'
```

> Example response

```json
{
  "message": "Successfully created person",
  "person": {
    "id": 123,
    "name": "Example person",
    "email": "example@gmail.com",
    "created_at": "2018-08-08T18:46:03.081Z",
  }
}
```

This endpoint will create a new person.

### HTTP Request

`POST http://nextplease.test/api/v1/people`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
name | string | The name of the person.
email | string | The email of the person.

## Update a person

> Example request

```shell
curl http://nextplease.test/api/v1/people/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"name":"New name"}' \
  -X PUT
```

> Example response

```json
{
  "message":"Successfully updated person",
  "person":{
    "id":123,
    "name":"New name",
    "email": "example@gmail.com",
    "created_at": "2018-08-08T18:46:03.081Z",
  }
}
```

This endpoint will update an existing person.

### HTTP Request

`PATCH http://nextplease.test/api/v1/people/<ID>`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
name | string | The name of the person.
email | string | The email of the person.

## Delete a person

> Example request

```shell
curl http://nextplease.test/api/v1/people/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -X DELETE
```

> Example response

```json
{
  "message":"Successfully deleted person"
}
```

This endpoint will delete a person.

### HTTP Request

`DELETE http://nextplease.test/api/v1/people/<ID>`
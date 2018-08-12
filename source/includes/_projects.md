# Projects

## Get all projects

> Example request

```shell
curl http://nextplease.test/api/v1/projects \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "title": "Example project",
    "content": "Description for example project",
    "public": true,
    "public_content": "This is the public description for example project",
    "created_at": "2018-08-08T18:46:03.081Z",
    "archived_at": null
  }
]
```

This endpoint retrieves all projects.

### HTTP Request

`GET http://nextplease.test/api/v1/projects`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the project.
title | string | This is the title of the project.
content | text | This is the description of the project.
public | boolean | This will be true if the project is publicly available. This is false by default.
public_content | text | This is the description that is shown on the public roadmap or changelog.
created_at | datetime | When the project was created.
archived_at | datetime | When the project was archived. Null if the project isn't archived.

## Get a specific project

> Example request

```shell
curl "http://nextplease.test/api/v1/projects/<ID>"
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
{
  "id": 123,
  "title": "Example project",
  "content": "Description for example project",
  "public": true,
  "public_content": "This is the public description for example project",
  "created_at": "2018-08-08T18:46:03.081Z",
  "archived_at": null,
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

This endpoint retrieves a specific project along with all associated requests and comments.

### HTTP Request

`GET http://nextplease.test/api/v1/requests/<ID>`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the project.
title | string | This is the title of the project.
content | text | This is the description of the project.
public | boolean | This will be true if the project is publicly available. This is false by default.
public_content | text | This is the description that is shown on the public roadmap or changelog.
created_at | datetime | When the project was created.
archived_at | datetime | When the project was archived. Null if the project isn't archived.

## Create a project

> Example request

```shell
curl http://nextplease.test/api/v1/projects \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"title":"Project title","content":"Description of the project."}'
```

> Example response

```json
{
  "message": "Successfully created project",
  "project": {
    "id": 123,
    "title": "Project title",
    "content": "Description of the project.",
    "created_at": "2018-08-12T03:00:31.879Z",
    "archived_at": null,
    "public_content": null,
    "public": false
  }
}
```

This endpoint will create a new project.

### HTTP Request

`POST http://nextplease.test/api/v1/projects`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
title | string | This is the title of the project.
content | text | This is the description of the project.

## Update a project

> Example request

```shell
curl http://nextplease.test/api/v1/projects/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -d '{"title":"New project title"}' \
  -X PUT
```

> Example response

```json
{
  "message":"Successfully updated project",
  "project":{
    "id":123,
    "title":"New project title",
    "content": "Description of the project.",
    "created_at": "2018-08-12T03:00:31.879Z",
    "archived_at": null,
    "public_content": null,
    "public": false
  }
}
```

This endpoint will update an existing project.

### HTTP Request

`PUT http://nextplease.test/api/v1/projects/<ID>`

### Parameters

Attribute | Type | Description
--------- | ------- | -----------
title | string | This is the title of the project.
content | text | This is the description of the project.

## Delete a project

> Example request

```shell
curl http://nextplease.test/api/v1/projects/<ID> \
  -H "Content-Type: application/json" \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV" \
  -X DELETE
```

> Example response

```json
{
  "message":"Successfully deleted project"
}
```

This endpoint will delete a project.

### HTTP Request

`DELETE http://nextplease.test/api/v1/projects/<ID>`

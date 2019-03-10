# Roadmap

## Get all roadmap items

> Example request

```shell
curl https://nextplease.io/api/v1/roadmaps \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "priority": 1,
    "stage_id": 1,
    "created_at": "2018-08-10T22:16:06.547Z",
    "roadmapable_type": "Request",
    "roadmapable": {
        "id": 123,
        "title": "Example request"
    }
  }
]
```

This endpoint retrieves all items on the roadmap.

### HTTP Request

`GET https://nextplease.io/api/v1/roadmaps`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the roadmap item.
priority | integer | Priority order of roadmap items from first to last.
stage_id | integer | Unique identifier for the stage this roadmap item belongs to.
created_at | datetime | When the item was added to the roadmap.
roadmapable_type | string | This tells you the type of object that is on the roadmap. For now, this can only be a "Request".

## Get all changelog items

> Example request

```shell
curl https://nextplease.io/api/v1/roadmaps/shipped \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "priority": 1,
    "stage_id": 1,
    "shipped_at": "2018-08-11T22:42:00.000Z",
    "created_at": "2018-08-10T22:16:06.547Z",
    "roadmapable_type": "Request",
    "roadmapable": {
        "id": 123,
        "title": "Example request"
    }
  }
]
```

This endpoint retrieves all items on the changelog.

### HTTP Request

`GET https://nextplease.io/api/v1/roadmaps/shipped`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the roadmap item.
priority | integer | Priority order of roadmap items from first to last.
stage_id | integer | Unique identifier for the stage this roadmap item belongs to.
shipped_at | datetime | When the roadmap item was marked shipped.
created_at | datetime | When the item was added to the roadmap.
roadmapable_type | string | This tells you the type of object that is on the roadmap. For now, this can only be a "Request".

## Get all stages

> Example request

```shell
curl https://nextplease.io/api/v1/stages \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "name": "Example stage",
    "order": 1,
  }
]
```

This endpoint retrieves all roadmap stages.

### HTTP Request

`GET https://nextplease.io/api/v1/stages`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the stage.
name | string | Name of the stage.
order | integer | Order of the stage, shown on the roadmap.

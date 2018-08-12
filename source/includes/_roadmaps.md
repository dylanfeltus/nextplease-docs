# Roadmap items

## Get all roadmap items

> Example request

```shell
curl http://nextplease.test/api/v1/roadmaps \
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
[
  {
    "id": 123,
    "priority": 1,
    "stage_id": 1,
    "shipped_at": null,
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

`GET http://nextplease.test/api/v1/roadmaps`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the roadmap item.
priority | integer | Priority order of roadmap items from first to last.
stage_id | integer | Unique identifier for the stage this roadmap item belongs to.
shipped_at | datetime | When the roadmap item was marked shipped.
created_at | datetime | When the item was added to the roadmap.
roadmapable_type | string | This tells you the type of object that is on the roadmap. Roadmap items can be "Project" or "Request" types.

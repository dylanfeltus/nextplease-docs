# Comments

## Get a specific comment

> Example request

```shell
curl "http://nextplease.test/api/v1/comments/<ID>"
  -H "X-User-Token: 4nxAn76-TumRoaexkDqV"
```

> Example response

```json
{
  "id": 123,
  "content": "This an example comment",
  "user_id": 1,
  "commentable_type":"Request",
  "commentable_id": 123,
  "created_at": "2018-08-08T18:46:03.081Z",
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

This endpoint retrieves a specific comment along with all replies.

### HTTP Request

`GET http://nextplease.test/api/v1/comments/<ID>`

### Attributes

Attribute | Type | Description
--------- | ------- | -----------
id | integer | Unique identifier for the comment.
content | text | Content of the comment.
user_id | integer | Unique identifier for the user who left this comment.
commentable_type | string | This tells you the type of object that this comment is attached to. Commentables can be "Request", "Project" or "Comment" types.
commentable_id | integer | Unique identifier of the commentable.

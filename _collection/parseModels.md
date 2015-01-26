---
header: parseModels
example: Collection.parseModels(response)
---

Loops each model in the collections response, each model object will then be returned by the [Models jsonKey](/model#jsonKey).

This is so the data can easily be formatted in the way Backbone is expecting if you're using an API that has keys for each attribute.

```js
// user model has jsonKey set to 'user'
// API response
[{
  user: {
    id: 1,
    name: 'Han Solo'
  },
}, {
  user: {
    id: 2,
    name: 'Chewbacca'
  }
}]

// result
[{
  id: 1,
  name: 'Han Solo'
}, {
  id: 2,
  name: 'Chewbacca'
}]
```

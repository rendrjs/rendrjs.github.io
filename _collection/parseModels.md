---
header: parseModels
example: Collection.parseModels(response)
---

Loops over each model in the collection's response.  Each model object will then be returned by the model's [parse](/model#parse) function.

If the `jsonKey` is set, Backbone can automatically parse models returned from an API that is formatted using the root keys.

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

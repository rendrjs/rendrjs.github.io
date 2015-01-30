---
header: parseModels
example: Collection.parseModels(response)
---

Loops over each Model in the Collection's response.  Each Model object will then be returned by the Model's [parse](/model#parse) function.

If the `jsonKey` is set, Backbone can automatically parse Models returned from an API that are formatted using the root keys.

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

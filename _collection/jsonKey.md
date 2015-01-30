---
header: jsonKey
example: Collection.jsonKey
---

**jsonKey** is the JSON root of the response from the API.  An API response with a root key will automatically be [parsed](#parse).

```js
Collection.jsonKey = 'user';
// expected data format from the API
// this will then be parsed and set the models attribute to the array
{
  users: [{
    id: 1,
    name: 'Tester'
  }]
}
```


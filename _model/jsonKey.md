---
header: jsonKey
example: Model.jsonKey
---

**jsonKey** is the JSON root of the response from the API.  An API response with a root key will automatically be [parsed](#parse).

```js
Model.jsonKey = 'user';
// expected data format from the API
// this will then be parsed and set onto the model
{
  user: {
    id: 1,
    name: 'Tester'
  }
}
```


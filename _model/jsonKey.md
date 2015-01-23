---
header: jsonKey
example: Model.jsonKey
---

**jsonKey** is the JSON root of the response from the API. This will automatically [parse](#parse) an API response with a root key.

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


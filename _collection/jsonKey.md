---
header: jsonKey
example: Collection.jsonKey
---

*jsonKey* is the JSON root of the response from the API. This will automatically [parse](#parse) an API response with a root key.

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


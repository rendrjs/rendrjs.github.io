---
header: summarize
example: Fetcher.summarize(modelOrCollection)
---

Returns a summary object of a collection or model.  This is used when hydrating views, and passing data from the server to the client.

Example Model Summary:

```js
{
  model: 'User',
  id: 1
}
```

Example Collection Summary:

```js
  collection: 'Users',
  ids: [1, 2, 3],
  params: { id: [1, 2, 3] },
  meta: { page: 0 }
```


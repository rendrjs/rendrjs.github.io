---
header: get
example: CollectionStore.get(collectionName, params, [callback])
---

Returns the collection from the store based on the collection name and it's [params](/collection#params).

You can also use the `get` function asynchronously by passing a `callback` function.
```js
// async
fetcher.collectionStore.get('users', {ids: [1,2,3]}, function (result) {
  // can access the users in the result
});

// sync
var result = fetcher.collectionStore.get('users', { ids: [1,2,3] })

```

---
header: get
example: CollectionStore.get(collectionName, params, [callback])
---

Returns the collection from the store based on the collection name and its [params](/collection#params).

You can also use the `get` function asynchronously by passing a `callback` function.

```js
// async
fetcher.collectionStore.get('UsersCollection', { ids: [1,2,3] }, function (result) {
  // do something with the users
});

// sync
var result = fetcher.collectionStore.get('UsersCollection', { ids: [1,2,3] })

```

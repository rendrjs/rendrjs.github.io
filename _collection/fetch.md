---
header: fetch
example: Collection.fetch([options])
---

Accepts options to override parameters as `options.data`. Will invoke the [Syncer's fetch](/syncer#fetch) method.  If an `options.data` is not provided it will use the original [params](#params) of the collection.

```js
// override
Collection.fetch({
  data: {
    ids: [1, 2]
  }
})

// use previously defined params
Collection.fetch()
```

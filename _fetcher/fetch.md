---
header: fetch
example: Fetcher.fetch(fetchSpec, [options], callback)
---

Fetches [Models](/model) or [Collections](/collection) according to the parameters defined in the `fetchSpec` and populates the corresponding ModelStore and/or CollectionStore.

Example `fetchSpec`:

```js
{
  user: {
    model: 'User',
    params: {id: 1},
    needsFetch: true,
    ensureKeys: ['id', 'name']
  },

  model: {
    model: 'Character',
    params: { name: 'Han Solo' }
  },

  starWarsCharacters: {
    collection: 'StarWarsCharacters',
    params: { film: 'Star Wars' }
  }
}
```

This `fetchSpec` will get two models (the User and Character models) and one collection (the StarWarsCharacters collection).

Extra options to pass to a `fetchSpec`:

- *needsFetch* - Allows you to force a fetch request
- *ensureKeys* - Ensures any stored data has all the required data, if not an API request will be made

The `callback` function will be called with an `error` and `results` from the fetch.  For an example callback function, check out the [Controller](/controller) documentation.

`options` *optional* Allows you to set caching information.  The defaults differ between client and server:  by default API responses are not written or read from the cache on the server, but both are true on the client.

Example `options`:

```js
var opts = {
  readFromCache: true,
  writeToCache: true
};

Fetcher.fetch(fetchSpec, opts, callback);
```

The `fetch` function will make an AJAX request if `readFromCache` is false **or** if the data does not exist in the ModelStore or CollectionStore.  If the data isn't found in the relevant store, it makes AJAX requests for each item defined in the `fetchSpec`.  **Note**:  These AJAX requests are run in parallel.

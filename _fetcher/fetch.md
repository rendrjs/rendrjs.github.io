---
header: fetch
example: Fetcher.fetch(fetchSpec, [options], callback)
---

`fetchSpec` is an object with the information to fetcher [Models](/model) or [Collections](/collection).

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

This `fetchSpec` will get two models, the User and Character models, and one collection, the StarWarsCharacters collection.

Extra options to pass a `fetchSpec`:

- *needsFetch* - Allows you to force a fetch request
- *ensureKeys* - Ensures any stored data has all the required data, if not an API request will be made

The `callback` function will be called with an `error` and `results` from the fetch.  The `error` argument will contain any errors when fetching data.  The `results` argument is an object of results from the API requests.  Each key is defined in the `fetchSpec` where the value is the response from the API.  For an example of what a callback function might look like, check out the [Contoller](/controller) documentation.

`options` *optional* Allows you to set caching information.  The defaults for the options differ from client and server.  By default API responses are not written or read from the cache on the server, but both are true on the client.

Example `options`:

```js
var opts = {
  readFromCache: true,
  writeToCache: true
};

Fetcher.fetch(fetchSpec, opts, callback);
```

The `fetch` function will make an AJAX request if `readFromCache` is false **or** if the data does not exist in the store.  By default on the client, the fetch request will check the corresponding store to see if the data exists, if it does no request is made and it simply returns the value in the store.  If the data isn't found it generates AJAX requests for each item defined in the `fetchSpec`.  **Note**: These AJAX requests are run in parallel.

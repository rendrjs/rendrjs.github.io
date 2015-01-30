---
header: fetch
example: App.fetch(spec)
---

Curries the function call for [Fetcher.fetch](/fetcher#fetch).  The spec is an object that is formatted to have the name of the result key, then the fetch information.

Example spec:

```js
var spec = {
  myModel: {
    model: 'ModelName',
    params: { id: 1 }
  },

  characters: {
    collection: 'Characters',
    params: { name: 'Han' }
  },

  // special model key for the view
  model: {
    model: 'User',
    params: { id: 5 }
  }

  // you can also set a collection to be the focus of the view
}
```

App.fetch requests generally take place in the [Controller](/controller), which will make the request for all the required data for a given page.  These `spec`s are also auto generated when you [lazy load](/view#fetchLazy) a view.

---
header: api
example: Collection.api
---

**api** is a configuration that allows you to change to a different API.  These APIs are configured to the [`dataAdapterConfig`](/app#config).  The configuration key for the host/protocol will automatically be set on the collection in the API-Proxy layer.  This allows you to talk directly to third party sites without having to worry about cross-site scripting.

```js
// DataAdapterConfig
dataAdapterConfig: {
  'github': {
    host: 'api.github.com',
    protocol: 'https'
  },
  'default': {
    host: 'my.site.com',
    protocol: 'https'
  }
}

// collection
module.exports = Base.extend({
  api: 'github'
});
```

If you don't provide an `api` it will automatically use the `default` key in the dataAdapterConfig.

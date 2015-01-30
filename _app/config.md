---
header: config
example: 
---

The options that can be passed into the Rendr App object.

- **dataAdapterConfig** Standard way of configuring the built-in [RestAdapter](/rest-adapter)
- **dataAdapter** _optional_ Allows you to override the default dataAdapter is the [RestAdapter](/rest-adapter) if this is set, the `dataAdapterConfig` is ignored
- **apiPath** _optional_ Root of the API proxy's virtual path. Anything after this root will be followed by a `-`. Example: `/api/-/path/to/resource`. Allows the proxy to intercept API routes. Can also be a full path to a remote API `http://api.myserver`. The default is set to: `api`
- **appData** _optional_ Pass any data that needs to be accessible by the client. Accessible from within your Handlebars context `app.attributes.myAttr`, and also within your views and models `this.app.attributes.myAttr`.
- **defaultEngine** _optional_ Tell the ViewEngine to load different file types. For example: `coffee`.  By default this is set to `js`.
- **entryPath** _optional_ Root path for the app. Default: `process.cwd() + '/'` (the current working directory)
- **errorHandler** _optional_ Callback for [Express.js errors](http://expressjs.com/guide.html#error-handling)
- **notFoundHandler** _optional_ Callback for [Express.js not found errors](http://expressjs.com/guide.html#error-handling)
- **viewEngine** _optional_ Provides a way to set a custom [Express.js ViewEngine](http://expressjs.com/api.html#app.engine)
- **viewsPath** _optional_ Override where the views are stored. This path is relative to `entryPath`. Default value is: `app/views`

Example configuration:

```js
var config = {
  dataAdapterConfig: {
    'default': {
      host: 'api.github.com',
      protocol: 'https'
    }
  },

  apiPath: '/api',
  appData: { myAttr: 'value'},
  dataAdapter: myDataAdapterInstance,
  defaultEngine: 'js',
  entryPath: process.cwd() + '/myapp',
  errorHandler: function (err, req, res, next){},
  notFoundHandler: function (req, res, next){},
  viewsPath: "/app/views"
};

rendr.createServer(config);
```

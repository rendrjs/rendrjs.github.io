---
header: config
example: 
---

The options that can be passed into the Rendr App object.

- **dataAdapterConfig** Standard way of configuring the built-in RestAdapter, which is a simple REST pass through.
- **dataAdapter** _optional_ Allows you to override the default dataAdapter.  The default is a simple REST pass through.  If the `dataAdapter` option is set, the `dataAdapterConfig` will be ignored.
- **apiPath** _optional_ Root of the API proxy's virtual path. Anything after this root will be followed by a `-`. Example: `/api/-/path/to/resource`. Allows the proxy to intercept API routes. Can also be a full path to a remote API `http://api.myserver`. The default is set to: `api`
- **appData** _optional_ Pass any data that needs to be accessible by the client.  You can access this data from within your Handlebars context as `app.attributes.myAttr`, and from within your views and models as `this.app.attributes.myAttr`.
- **defaultEngine** _optional_ Tell the ViewEngine to load different file types. For example: `coffee`.  By default this is set to `js`.
- **entryPath** _optional_ Root path for the app. Default: `process.cwd() + '/'` (the current working directory)
- **errorHandler** _optional_ Callback for [Express.js errors](http://expressjs.com/guide/error-handling.html)
- **notFoundHandler** _optional_ Callback for [Express.js not found errors](http://expressjs.com/guide/error-handling.html)
- **viewEngine** _optional_ Set a custom [Express.js ViewEngine](http://expressjs.com/api.html#app.engine)
- **viewsPath** _optional_ Override where the views are stored. This path is relative to `entryPath`. Default value is: `app/views`
- **baseLayoutName** _optional_ Set a custom name for the base template file of the app. For example `myLayout`. The default value is set to `__layout`.

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

### Template Adapters

Provides a way for Rendr to utilize custom html template engines (see also Template Engines section below).  Rendr's [ViewEngine](https://github.com/rendrjs/rendr/blob/master/server/viewEngine.js) will delegate to the [Template Adapter](https://github.com/rendrjs/rendr-handlebars/blob/master/index.js). You can build your own to provide your template engine of choice (i.e. Jade, Underscore templates, etc).

####Available Template Adapters

- [rendr-handlebars](https://github.com/rendrjs/rendr-handlebars) - [Handlebars.js](https://github.com/wycats/handlebars.js) support.  This is the default adapter.

- [rendr-emblem](https://github.com/modalstudios/rendr-emblem) - [Emblem.js](https://github.com/machty/emblem.js/) with [Handlebars.js](https://github.com/wycats/handlebars.js) fallback support.


####Using Custom Adapters

You can tell Rendr which Template Adapter to use.  This represents the node-module that contains the adapter.

```js
// /app/app.js

module.exports = BaseApp.extend({
  defaults: {
    templateAdapter: 'rendr-emblem'
  }

});

```

### Template Engines

While Template Adapters provide the layer of abstraction that allow you to use your favorite template engine in a Rendr app, the Template Engine option itself will tell the app which version to use exactly. 
The default is set to be Handlebars, which is currently supported by the Rendr-handlebars adapter until version 2.0.0.
**When setting up your Rendr app, you'll need to add your Template Engine of choice to package.json.**
 
E.g.
 
```js
// /package.json

"dependencies": {
  ...
  "express": "^4.12.0",
  "handlebars": "^2.0.0"
  "qs2": "~0.6.6",
  ...
},
  
```

####Using Custom Template Engines

You can tell Rendr which Template Engine to use.  This represents the node-module that contains the engine.

```js
// /app/app.js

module.exports = BaseApp.extend({
  defaults: {
    templateEngine: 'handlebars'
  }

});

```

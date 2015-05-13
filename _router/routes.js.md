---
header: routes.js
example: FILE `app/routes.js`
---

This file stores the mapping between a URL route and a [controller action](/controller#action).

Example `routes.js` file:

```js
module.exports = function(addRoute) {
  addRoute('users/login', 'users#login', { role: admin });
  addRoute('users/:id', 'users#show');
  addRoute('test', {controller: 'test', action: 'index'});
  addRoute('testRedirect', 'testRedirect#index', { redirect: '/foo' });
  addRoute('testRoles', 'testRole#index', { role: 'admin' }});
  addRoute(/^\/regexp\/(foo|bar)/, 'test#regexp');
};
```

`addRoute` is a callback function defined in Rendr to add the route to a list of available routes.

The callback function takes 3 parameters:

1. The URL for the route, which can also be a regular expression
2. The The controller [name](/controller#name) and [action](/controller#action) can be specified either by a shorthand string notation, or by an object:
    - Shorthand: 'controllerName#action'
    - Object: `{controller: 'controllerName', action: 'action'}`

3. *optional* An object of options to pass to the router.  If the object contains a redirect, no controller information is required. The options object can also add headers to the content returned from the Express server by adding them to a headers element, e.g.:

```
var headers = {
  'Vary': 'User-Agent',
  'Cache-Control': 'no-transform,public,max-age=300,s-maxage=900',
  'ETag': '12345678'
};
addRoute('testRoles', 'testRole#index', {role: 'admin', headers: headers}});
```

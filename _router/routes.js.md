---
header: routes.js
example: FILE `app/router.js`
---

The `routes.js` file stores the mapping between a URL route and the [controller action](/controller#action).

Example `routes.js` file:

```js
module.exports = function(addRoute) {
  addRoute('users/login', 'users#login', { role: admin });
  addRoute('users/:id', 'users#show');
  addRoute('test', 'test#index');
  addRoute('testRedirect', 'testRedirect#index', { redirect: '/foo' });
  addRoute('testRoles', 'testRole#index', { role: 'admin' }});
  addRoute(/^\/regexp\/(foo|bar)/, 'test#regexp');
};
```

`addRoute` is a callback function defined in Rendr to add the route to a list of available routes.

The callback function takes 3 parameters:

- The URL for the route, this can also be a regular expression to match
- The controller [name](/controller#name) and the [action](/controller#action), 'controllerName#action'
- *optional* An object of options to pass to the router.  If the object contains a redirect, no controller information is required.

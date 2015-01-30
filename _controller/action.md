---
header: action
---

The action is defined in the controller file.  It is a key in the `module.exports` object.

Example:

```js
// content of users_controller.js
module.exports = {
  index: function (params, callback) {
    callback()
  }
};
```

The example above will have add the `index` action to the `users_controller`.  To hookup the controller's action to a route simply add `addRoute('/users', 'users#index')` to the [app/routes.js](/router#routes.js) file.

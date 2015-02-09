---
layout: content
title: Controller - RendrJS
---

# Controller

Controllers are an addition to Rendr that do not exist in Backbone.  Controllers define functions (known as [actions](#action)) that the [router](/router) will invoke when a URL is visited.  This allows us to have a cleaner router.

Controllers have no base class, as they are simply objects containing functions.  Simply create files in the `controllers/` directory of your application and follow the naming convention: `<name>_controller.js`.  The [name](#name) is how the router will know which file to open.  The keys of the object being exported are the [actions](#action) for a controller.

Example Controller:

```js
// controllers/users_controller.js
module.exports = {
  index: function(params, callback) {
    var spec = {
      collection: { collection: 'Users', params: {} }
    };

    this.app.set('title', 'Users');
    this.app.fetch(spec, callback);
  },

  show: function(params, callback) {
    var spec = {
      model: {
        model: 'User', params: { id: params.id }
      }
    };

    this.app.fetch(spec, function (err, results) {
      // return if there is an error fetching the user
      if (err) return callback(err);

      // set the title of the page to the users name
      this.app.set('title', results.model.get('name'));

      // render the page with the results from the fetch
      callback(null, results);
    }.bind(this));
  }
};
```

The above example creates a controller with two actions, `index` and `show`.  The `index` action will display all the users, and the `show` action will show a specific user by their id.

Example [routes.js](/router#routes.js) file:

```js
module.exports = function(addRoute) {
  addRoute('/users', 'users#index');
  addRoute('/users/:id', 'users#show');
};
```

Note how the `routes.js` file will match the controller's [name](#name) and the [action](#action).

{% include pageDoc.html name="controller" %}


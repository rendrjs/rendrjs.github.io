---
header: constructor
example: new Collection([models], [options])
---

The constructor creates a new instance of a Collection.  To customize your constructor, create an `initialize` function on the child class, this function will be invoked once the parents constructor method is completed. See [Backbone's documentation](http://backbonejs.org#Collection-constructor) for more information.

The `models` parameter is an array of [*Models*](/model).

The options are the same as the standard [Backbone.Collection](http://backbonejs.org#Collection-constructor), but in Rendr it also expects an `app` object.  The [Rendr App](/app) instance must be passed, in order to sync data to the API.


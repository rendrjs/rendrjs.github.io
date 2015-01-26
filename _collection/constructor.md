---
header: constructor
example: new Collection([models], [options])
---

The constructor creates a new instance of a Collection.  For creating a customized constructore, then create an `initialize` function, which is called by the constructor.

The models parameter is an array of [*Models*](/model).

The options are the same as the standard [Backbone.Collection](http://backbonejs.org#Collection-constructor), but in this case we are expecting an `app` attribute to be attached to the options.  The `app` attribute is the instance of the [Rendr App](/app) object.  This is required for syncing data to the API.


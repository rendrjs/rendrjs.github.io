---
header: constructor
example: new Model([attributes], [options])
---

The **constructor** will create an instance of a Rendr Model.  `options` expects a reference to the `app` object, which is required for the [Syncer](/syncer) to work.  The constructor invokes the parent Backbone initialization, and finally stores the instance in the model store.

The `attributes` variable is the data you want the model to store.  The `options` are additional options you wish to pass into the model, they are saved on the model as `this.options`.  These are the same arguments you pass to [Backbone.Model](http://backbonejs.org#Model-constructor).

To add functionality to the constructor, add an `initialize` function. This allows you to hook into the Model creation flow.  For more information about how to override `initialize` checkout [Backbones documentation](http://backobnejs.org#Model-constructor).


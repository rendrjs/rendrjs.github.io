---
header: constructor
example: new Model([attributes], [options])
---

The **constructor** will create an instance of a Rendr Model.  The options are expecting a reference to the app object, this is used to hook into the sync functionality.  The constructor also invokes the parent Backbone initialization, and finally stores the instance in the model store.

To add functionality to the constructor, add an `initialize` function.  This is pattern allows for any default functionality to run, while still being able to create a custom constructor.

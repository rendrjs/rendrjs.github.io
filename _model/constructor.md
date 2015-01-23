---
header: constructor
example: new Model([attributes], [options])
---

The **constructor** will create an instance of a Rendr Model.  The options are expecting a reference to the app object, this is used to hook into the sync functionality.  The constructor also invokes the parent Backbone initialization, and finally stores the instance in the model store.


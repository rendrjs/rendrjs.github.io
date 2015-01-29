---
header: constructor
example: new Model([attributes], [options])
---

The **constructor** will create an instance of a Rendr Model.  The options takes a reference to the app object, which is required for the Syncer to work.  The constructor invokes the parent Backbone initialization, and finally stores the instance in the model store.

To add functionality to the constructor, add an `initialize` function.  Any default functionality will still run.

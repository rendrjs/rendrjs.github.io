---
header: store
example: Model.store()
---

Saves the data to the model store.  The fetch function will retrieve data from the store first when the views are being constructed, thus reducing the number of requests to the server.

By default, `store` is triggered on the `change` event of the model's `idAttribute`.  This means that modifying the ID will automatically store the data again, so you *don't* need to set up a `change` event on the entire model.

This function invokes the [ModelStore.set](/model-store#set) function with the model.

---
header: store
example: Model.store()
---

This will save the data to the model store.  This data is retrieved when the veiws are being constructed.  This saves on requests as well, as the fetch function will check the store before creating the AJAX request to the server.  Store also has a default trigger setup on the `change` event of the `idAttribute`.  This means, if you modify the ID it will re-store the data.  Since the store is referencing the instance of the model, you *don't* need to setup a change event on the entire model, as it will get those changes automatically.



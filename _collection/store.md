---
header: store
example: Collection.store()
---

Stores the collection in the [Collection Store](/collection-store), and each of the models in the [Model Store](/model-store).

The lookup key is set to the `collectionName:params:` in the store, so that any set of parameters will only be requested from the server once.  This function also automatically populates the model store, thus eliminating any additional requests for those models.

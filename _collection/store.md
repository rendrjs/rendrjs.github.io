---
header: store
example: Collection.store()
---

Stores the collection in the [Collection Store](/collection-store), and each of the models in the [Model Store](/model-store).

The lookup key is set to the `collectionName:params:` in the store.  This allows us to only request data from the server once, by automatically populating the model store, it also will skip any additional requests for those models.

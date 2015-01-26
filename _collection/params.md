---
header: params
example: Collection.params
---

`params` is special attribute on a collection where you set fetching parameters.  These parameters are used to identify collections in Rendr.  Identification of a collection is used to store the data in the [CollectionStore](/collection-store)

When you set params in the options of a constructor, they are automatically set to the Collection as the `.params` attribute.

When you call [Collection.fetch](#fetch), it will apply these parameters to the GET request to the API.

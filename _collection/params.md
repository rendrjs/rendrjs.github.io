---
header: params
example: Collection.params
---

`params` stores the parameters that will be used to query for the models in the Collection.  These parameters are used to identify Collections in the [CollectionStore](/collection-store).  When you call [Collection.fetch](#fetch), it will apply these parameters to the GET request to the API.

You can automatically set parameters to the Collection as the `.params` attribute by passing them in the options of the Collection's [constructor](#constructor).

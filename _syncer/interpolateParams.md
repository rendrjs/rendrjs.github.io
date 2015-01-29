---
header: interpolateParams
example: Syncer.interpolateParams(modelOrCollection, url, params)
--- 

This will interpolate the url strings, for instance if the url you have set on a model is: `/model/:attr`, and the model has the value `1` for the `attr` attribute, the resulting url will be `/model/1`.

This function makes it so we can easily change the url parameters based on attributes in the model / collection.

If the this is interpolating a collection, it will check the options of the collection for the data to interpolate.


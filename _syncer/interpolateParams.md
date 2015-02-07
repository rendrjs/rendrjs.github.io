---
header: interpolateParams
example: Syncer.interpolateParams(modelOrCollection, url, params)
--- 

This will interpolate the url strings.  For instance if the url you have set on a model is: `/game/:category`, and the game has the value `dice` for the `category` attribute, the resulting url will be `/game/dice`.

This function enables us to easily change the url parameters based on attributes in the model / collection.  If interpolating a collection, it will check the collection's options for the data to interpolate.


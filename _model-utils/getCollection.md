---
header: getCollection
example: ModelUtils.getCollection(path, [models], [options], [callback])
---

Factory method for collections. Given the path of a collection, this function will return an instance of that collection. This will also add the `models` to that collection, and set any `options` to the collection.  `callback` allows the method to be called asynchronously. 

**path** The path to the collection.  For example: `my_collection`, would return an instance of a collection stored in `app/collections/my_collection.js`

**models** _optional_ An array of models to store in the collection.

**options** _optional_ Options for the [collection constructor](/collection#constructor).

**callback** _optional_ Callback function to be invoked once the instance is created.  If a callback is not passed in, this will return the instance instead.

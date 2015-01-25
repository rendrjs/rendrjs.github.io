---
header: parse
example: Model.parse(response, [options])
---

The **parse** method is called when data is returned from a [fetch](http://backbonejs.org#Model-fetch) request.

The *response* is a json object, and the value returned from this function will be set as the attributes on the model.  If your API is returning a root object in the key, you can set the [jsonKey](#jsonkey) to return the attributes, withouth having to override the default functionality.



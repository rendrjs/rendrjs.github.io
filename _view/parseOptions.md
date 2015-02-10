---
header: parseOptions
example: View.parseOptions(options)
---

This function populates the [this.options](#options) attribute, setting any required options on the view instance.  It will also create an instance of a [model](/model) or [collection](/collection) if the corresponding data is passed in.

```js
var view = new View({
  app: myApp, // some Rendr app object
  model: {
    id: 1,
    name: 'Luke Skywalker'
  },
  model_name: 'Character'
});

/*
/* view.model will be an instance of the 'Character' model
 * with the attributes: id = 1, and name = Luke Skywalker
 */
```

The same can be done with a collection, with the keys `collection` and `collection_name`.

If you pass in an instance of a model or collection in the `model` or `collection` attribute, it will simply set the view property to that instance.

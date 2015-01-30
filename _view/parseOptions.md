---
header: parseOptions
example: View.parseOptions(options)
---

This function populates the [this.options](#options) attribute. It sets any of the required options to the view instance.  It will also create an instance of a [model](/model) or [collection](/collection) if the corresponding data is passed in.

```js
var view = new View({
  app: myApp, // some Rendr app object
  model: {
    id: 1,
    name: 'Luke Skywalker'
  },
  model_name: 'Character'
});

// view.model will be an instance of the 'Character' model
// it will have the attributes: id = 1, and name = Luke Skywalker
```

The same can be done with a collection, except the keys are `collection` and `collection_name`.

If the `model` or `collection` attributes are an instance of a model or collection, it will simply set the view property to that instance.

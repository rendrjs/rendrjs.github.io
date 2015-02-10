---
header: constructor
example: new View([options])
---

Creates a new instance of the View object.  A required option is [app](/app) which is used in many helper functions throughout the view.

The constructor will also intelligently retrieve [model](/model) and [collection](/collection) information.  If you pass a JSON object with an id and give it the `collection_name` or `model_name` options, it will retrieve that data from the corresponding store and set the populated model / collection as an attribute on the view.  For more information on parsing the model and collection attributes see [parseOptions](#parseOptions).

You can set additional initialization information in the view constructor by adding an `initialize` function, just as in [Backbone's initialization](http://backbonejs.org/#View-constructor).

Another special option is `template_name`, where you can set a different template for the view.  By default this is `undefined`.

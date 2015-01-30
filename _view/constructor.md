---
header: constructor
example: new View([options])
---

Creates a new instance of the View object.  A required option is [app](/app) which is used in many of the helper functions throughout the view, and entire application.

The constructor will also intelligently retrieve [model](/model) and [collection](/collection) information.  If you pass a JSON object with an ID and give it the `collection_name` or `model_name` options, it will retrieve that data from the corresponding store and set the inflated model / collection as the view attribute.  For more information on parsing the model and collection attributes see [parseOptions](#parseOptions).

The view constructor can have additional initialization information set by adding an `initialize` function.  This is the same pattern developed in [Backbone's initialization](http://backbonejs.org/#View-constructor).

Another special option is `template_name`.  This allows a point to hook in at to give a view a different template, by default this is `undefined`.

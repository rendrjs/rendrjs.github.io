---
header: parse
example: Collection.parse([response], [modifyInstance])
---

Parse the data being returned from an API.  By setting a [jsonKey](#jsonKey) attribute it will parse and return the object as you would expect without having to override the function.  This will call the [parseModels](#parseModels) method by default.

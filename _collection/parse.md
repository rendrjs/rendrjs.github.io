---
header: parse
example: Collection.parse([response], [modifyInstance])
---

Parse the data that is returned from an API `fetch`.  If you set a [jsonKey](#jsonKey) attribute on the collection, it will parse the objects as you would expect without having to override this function.  This calls the [parseModels](#parseModels) method by default.

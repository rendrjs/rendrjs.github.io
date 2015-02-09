---
header: find
example: ModelStore.find(modelName, attrs)
---

Returns the first instance found that matches the `modelName` and `attrs` sent.  The `modelName` is the name of the model, the `attrs` is an object of parameters to search on.

Example:
```js
modelStore.find('Media', { type': 'photo', 'id': 16 })
```

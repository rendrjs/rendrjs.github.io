---
header: lazyErrorCallback
example: View.lazyErrorCallback(err)
---

*Client-side only*  This is callback function is invoked once the [fetchLazy](#fetchLazy) has been completed in the case of an error. This function is meant to be overridden on a view where you want handle an error when the view is lazy loaded.  The first parameter is the error that was received from the server allowing you to handle errors according to the status code or error text from the server.

```js
module.exports = BaseView.extend({
  lazyErrorCallback: function(err) {
    if (err.statusCode === 404) { this.remove(); }
  }
});
```

The above code is an example of how you might want to handle an entity not found in a lazy-loaded view.  To override the success handler see the [lazyCallback](#lazyCallback) function.

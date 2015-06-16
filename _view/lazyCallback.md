---
header: lazyCallback
example: View.lazyCallback(results)
---

*Client-side only* Callback function which is invoked on the successful request for data from the server in a [fetchLazy](#fetchLazy) request. The function has a `results` parameter which is the object returned from the fetch request.  By default this function will simply [render](#render) the view, inserting the information for the view into the DOM.

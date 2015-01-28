---
header: fetchLazy
example: View.fetchLazy()
---

*Client-side only* To lazy load a view set the `lazy` option to true.

<pre><code>var view = new View({
  'lazy': true,
  'fetch_params': { id: 1 },
  'model_name': 'TestModel'
});</code></pre>

View options for enabling lazy loading:

- `lazy` - Set this to true to stop the server from trying to render the HTML server-side.
- `fetch_params` - an object of parameters to send to the API for the model or collection
- `model_name` - This is used to make the fetch request for a model with the given parameters
- `collection_name` - If you're requesting a collection, this is the name of the collection for the view.

When the request begins, the `loading` class is added to the view, and triggers the `loading` event.  [preRender](#preRender) is also invoked before the fetch request to the server.  Once the data is retrieved from the server, if the view is still attached to the DOM, it will parse the results and [render](#render) the view.

---
header: getHtml
example: View.getHtml()
---

Returns the HTML for a View, including the wrapper defined in the view.  This invokes [getInnerHtml](#getInnerHtml) then builds a wrapper element using the attributes from [getAttributes](#getAttributes).

```js
var View = RendrView.extend({
  tagName: 'a',
  className: 'text-primary'
});

var view = new View({
  'additional-option': 'test'
});

view.getHtml();
```

The Result: `'<a class="text-primary" data-additional-option="test">/* template */</a>'`

This function is expected to only be used on the server.

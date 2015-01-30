---
header: getTemplateData
example: View.getTemplateData()
---

Returns a JSON object of the data available for the template.  This data includes a JSON version of the model or collection attributes and all of the view's [options](#options).

Overriding this function allows us to introduce additional variables that need to be computed at run time.

```js
View = RendrView.extend({
  getTemplateData: function () {
    var data = RendrView.prototype.getTemplateData.call(this);

    return _.extend({
      now: (new Date).getTime()
    }, data);
  }
});

// Our templates we have access to the `now` variable, which is set to epoch time.
```

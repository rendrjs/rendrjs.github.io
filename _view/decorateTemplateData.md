---
header: decorateTemplateData
example: View.decorateTemplateData(data)
---

This function takes the result from [getTemplateData](#getTemplateData) and applies special properties to the data for the view.  The special properties are `_app`, `_view`, `_model`, and/or `_collection`.  These special properties are the instance variables for each of the options set on the view.

These are generally used in view helper functions, and for passing the instances to sub-views.

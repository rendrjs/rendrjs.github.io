---
header: render
example: View.render()
---

*Client-side only*, expects the DOM to present.

This will call [getInnerHtml](#getInnerHtml) to get the HTML for the view.  It will then set the attributes on the element, and finally invoke the [postRender](#postRender) hooks.

In general, you should never need to override the `render` function, instead use the [postRender](#postRender).

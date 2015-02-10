---
header: render
example: View.render()
---

*Client-side only* Expects the DOM to be present.

This calls [getInnerHtml](#getInnerHtml) to get the HTML for the view, then sets the attributes on the element, and finally invokes the [postRender](#postRender) hooks.

In general, you should never need to override the `render` function – use [postRender](#postRender) instead.

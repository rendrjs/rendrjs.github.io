---
header: postRender
example: View.postRender
---

*Client-side only*, this is only invoked after the [render](#render) function is called.  By default `postRender` is a no-op.  If you need anything to happen after rendering a view, it should be in this overridden function.  For instance, jQuery plugins should be hooked up in this function.

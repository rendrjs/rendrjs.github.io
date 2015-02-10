---
header: postRender
example: View.postRender
---

*Client-side only*  This is only invoked after [render](#render)ing or [attach](#attach)ing the view.  By default `postRender` is a no-op.  If anything needs to happen after rendering a view, it should go in this overridden function.  For instance, jQuery plugins should be initialized here.

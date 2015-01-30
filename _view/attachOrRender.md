---
header: attachOrRender
example: View.attachOrRender(element, parentView)
---

This is invoked when View is hydrating the [childViews](/#childViews).  This will inspect the element and check to see if the view is lazy loaded or already attached.  Hydration is the step where the HTML has been loaded by the server, or a view is creating an instance of a child view using a [template adapter](/template-adapters).

If neither of those are true, then it will see if the `data-render` attribute is set on the element. If it is, it will invoke the [render](#render) function.  If not, it will call the [attach](#attach) function on the element.

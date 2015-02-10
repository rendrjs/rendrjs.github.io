---
header: attachOrRender
example: View.attachOrRender(element, parentView)
---

This is invoked when View is [hydrating](/fetcher/#hydrate) the [childViews](#childViews).  This inspects the element to see if the view is lazy loaded or already attached.  If neither of those are true, then it will check if the `data-render` attribute is set on the element.  If it is, it will invoke the [render](#render) function.  Otherwise it will call the [attach](#attach) function on the element.

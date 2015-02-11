---
header: getInnerHtml
example: View.getInnerHtml()
---

Turns the view's template into a string of HTML, without the wrapper element defined in the view itself.

This function invokes the [preRender](#preRender) hook, which ensures that `preRender` is invoked on client and server.

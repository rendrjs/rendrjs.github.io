---
header: getInnerHtml
example: View.getInnerHtml()
---

Turns the view's template into a string of HTML, without the wrapper element defined in the view itself.

This will invoke the [preRender](#preRender) hook. Having the preRender invoked in `getInnerHtml` will ensure that it is invoked on client and server.

---
header: attach
example: View.attach()
---

This is invoked when the HTML has already been rendered by the server, and it invokes the [preRender](#preRender) and [postRender](#postRender) functions to setup accessors and any additional bindings for the view. Finally, it triggers the `attach` event.


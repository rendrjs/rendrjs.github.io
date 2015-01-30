---
header: name
---

All controllers are required to have the `_controller.js` post-fix.  The name of the controller is the filename before the post-fix.

For example: `users_controller.js` has the name `users`.

This is a convention, and doesn't actually have an attribute stored, the [router](/router) uses it to generate the handler in [addRouteDefinition](/router#addRouteDefinition).

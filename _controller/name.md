---
header: name
---

All controllers are required to have the `_controller.js` postfix.  The name of the controller is the filename before the postfix.

For example:  `users_controller.js` has the name `users`.

The [router](/router) uses this naming convention to generate the handler in [addRouteDefinition](/router#addRouteDefinition), but a `name` attribute isn't actually stored.

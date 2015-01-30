---
header: addRouteDefinition
example: Router.addRouteDefinition(route)
---

The route is formatted as an array, `['url', 'controller#action', { options }]`.  This creates a route and a callback for each route which invokes the [controller action](/controller#action).

Once the route has been created, the `route:add` event is triggered with an array of route data.


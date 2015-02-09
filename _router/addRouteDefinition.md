---
header: addRouteDefinition
example: Router.addRouteDefinition(route)
---

The route is formatted as an array: `['url', 'controller#action', { options }]`.  This function creates a route and a callback for it that invokes the associated [controller action](/controller#action).

Once the route has been created, the `route:add` event is triggered with an array of route data.


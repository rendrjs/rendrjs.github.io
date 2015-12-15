---
header: remove
example: View.remove()
---

Removes references in a view – removes all the child views, cleans up references to other views, sets `viewing` to false, removes the view from the DOM, and removes event listeners bound using Backbone [events](http://backbonejs.org#View-extend) or [listenTo](http://backbonejs.org#Events-listenTo).

This is invoked automatically on all the child views when the parent is removed.  The deconstrution of all views is also started when changing pages.

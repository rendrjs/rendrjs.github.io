---
layout: content
title: "Collection - RendrJS"
---

# Collection

Like in Backbone, collections are ordered sets of models.  You can use collections to delegate events for a group of models, listen to adding or removing of models from the set, and sync those sets with a server.  The major additions Rendr provides to Backbone is the [Collection Store](/collection-store) and the ability to sync the collection in the same fashion on client or server.

Note, all functions in the [Backbone.Collection](http://backbonejs.org#Collection) work, so make sure to checkout their documentation to see _all_ of the neat features you can do with this object.

{% for doc in site.collection %}
  <h2 id="{{doc.header}}">
    <a href="#{{doc.header}}">{{ doc.header }}</a>
    <span>{{ doc.example }}</span>
  </h2>

  <hr />
  {{doc.content}}
{% endfor %}


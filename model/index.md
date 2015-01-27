---
layout: content
title: "Model - RendrJS"
---

# Model

Rendr models are extenions on [Backbone Models](http://backbonejs.org#Model).  They are configured to run on the client and server, however some of the funcitonality works a little different between the two.  Ideally in a project you don't need to worry about these changes, but here's some documentation on how they function and some of the differences between the two states that they'll be running in.

The model also mixins the **[syncer](/syncer)** to encapsulate the logic for fetching data from an API on the client or the server.

{% for doc in site.model %}
  <h2 id="{{doc.header}}">
    <a href="#{{doc.header}}">{{ doc.header }}</a>
    <span>{{ doc.example }}</span>
  </h2>

  <hr />
  {{doc.content}}
{% endfor %}


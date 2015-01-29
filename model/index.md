---
layout: content
title: "Model - RendrJS"
---

# Model

Rendr models are extension on [Backbone Models](http://backbonejs.org#Model).  They are configured to run on the client and server, however some of the functionality works a little different between the two.  Ideally in a project you don't need to worry about these changes, but here's some documentation on how they function and some of the differences between the two states that they'll be running in.

The model also mixins the **[syncer](/syncer)** to encapsulate the logic for fetching data from an API on the client or the server.

{% include pageDoc.html name="model" %}

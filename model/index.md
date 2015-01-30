---
layout: content
title: "Model - RendrJS"
---

# Model

Rendr models extend [Backbone Models](http://backbonejs.org#Model).  They are configured to run on the client and server, though some of the functionality works a little different between the two.  You won't normally need to worry about these differences in your project.

The model also mixes-in the **[syncer](/syncer)** functionality for fetching data from an API on the client or the server.

{% include pageDoc.html name="model" %}

---
layout: content
title: "Fetcher - RendrJS"
---

# Fetcher

The Fetcher is initialized during the [app](/app) initialization.  The class is designed to fetch data from an API on the client or server.  It is attached to the app object and initializes the [Model Store](/model-store) and the [Collection Store](/collection-store).  It also mixes in the [Backbone.Events](http://backbonejs.org#Events) to allow you to trigger the events on client or server the same way you would in Backbone.

{% include pageDoc.html name="fetcher" %}


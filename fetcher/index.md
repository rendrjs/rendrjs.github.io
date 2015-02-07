---
layout: content
title: "Fetcher - RendrJS"
---

# Fetcher

The Fetcher is initialized during the [app](/app) initialization and is attached to the app object.  This class is designed to fetch data from an API on the client or server.  It initializes the [Model Store](/model-store) and [Collection Store](/collection-store), and mixes in the [Backbone.Events](http://backbonejs.org#Events) to allow you to trigger events on client or server the way you would in Backbone.

{% include pageDoc.html name="fetcher" %}


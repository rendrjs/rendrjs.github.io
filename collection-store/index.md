---
layout: content
title: "Collection Store - RendrJS"
---

# Collection Store

The collection store is created to store collections in memory.  This will reduce the number of requests to the API by saving the results from the first API request.  The Collection Store also populates the [Model Store](/model-store), by adding each of the collection's models to it.  Generally, this does not need to be modified, and it is instantiated by the [app](/app) during the [app initialization](/app#constructor).

{% include pageDoc.html name="collection-store" %}

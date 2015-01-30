---
layout: content
title: "Collection Store - RendrJS"
---

# Collection Store

The collection store is created to store collections in memory.  This will reduce the number of requests to the API by saving the results from the first API request.  The Collection Store also populates the [Model Store](/model-store), by adding each of the collection's models to it.  Generally, this does not need to be modified, and it is instantiated by the [app](/app) during the [app initialization](/app#constructor).

The Collection Store is attached to the [Fetcher](/fetcher) class.  This is so when you make a request through the fetcher, it will check the store before continuing the request.

{% include pageDoc.html name="collection-store" %}

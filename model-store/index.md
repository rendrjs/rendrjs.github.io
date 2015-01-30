---
layout: content
title: "Model Store - RendrJS"
---

# Model Store

The Model Store is created to make a cache in memory, specifically for the client.  This will help reduce the number of client-side requests by checking to see if the data is in the store before making a fetch request.  Generally, this does not need to be modified, and it is instantiated by the [app](/app) during the [app initialization](/app#constructor).

The Model Store is attached to the [fetcher](/fetcher) class.  This allows the fetcher to easily get verify if data is in the store or not, before making the AJAX request to the API.

{% include pageDoc.html name="model-store" %}

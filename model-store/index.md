---
layout: content
title: "Model Store - RendrJS"
---

# Model Store

The Model Store is created to make a cache in memory, specifically for the client.  This will help reduce the number of client-side requests by checking to see if the data is in the store before making a fetch request.  Generally, this does not need to be modified, and it is instantiated by the [app](/app) during the [app initialization](/app#constructor).

{% include pageDoc.html name="model-store" %}

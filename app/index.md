---
layout: content
title: App - RendrJS
---

# App

The App is a specialized [Model](/model).  A lot of the choices between client / server happen in the app. Here are some of its major features:

- Defines the template adapter
- Defines the template engine
- Initializes the client / server [router](/router)
- Initializes the [fetcher](/fetcher)
- Initializes [modelUtils](/model-utils)
- Initializes the app view, which in turn will initialize all views in use
- [Starts](#start) the client-side [router](/router)
- [Bootstraps the data](#bootstrapData) from the server into the client

{% include pageDoc.html name="app" %}


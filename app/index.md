---
layout: content
title: App - RendrJS
---

# App

The App is a specialized [model](/model).  The app is the place where a lot of the choices between client / server happen. Here are some of the major features of the app:

- Defines the template adapter
- Initializes the client / server [router](/router)
- Initializes the [fetcher](/fetcher)
- Initializes [modelUtils](/model-utils)
- Initializes the app view, which in turn will initialize all views in use
- [Starts](#start) the client-side [router](/router)
- [Bootstraps the data](#bootstrapData) from the server into the client

{% include pageDoc.html name="app" %}


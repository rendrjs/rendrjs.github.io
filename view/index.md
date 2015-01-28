---
layout: content
title: "View - RendrJS"
---

# View

Views are the most powerful addition with Rendr.  They have the ability to render HTML on the client or the server.  This has a huge impact on performance.  Namely, with SEO. We can now render the same HTML on the client or the server, allowing web crawlers to work the same way a client-side Backbone application would.

Rendr.View also hides a lot of the inner workings, simply invoke the [render](#render) method of a view and it will re-render the template with the current state of the data and replace the HTML for you.  There are also pre and post render hooks; [preRender](#preRender) and [postRender](#postRender).

Another performance boost comes with 'lazy-loading' views.  The views that don't effect SEO or are secondary to data are prime views to lazy-load.  When you lazy-load a view, it will wait to fetch data from the API until the page is loaded client-side.  After fetching the data, it will automatically render the component it was defined.

{% include pageDoc.html name="view" %}


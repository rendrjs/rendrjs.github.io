---
layout: content
title: "View - RendrJS"
---

# View

Views are the most powerful addition in Rendr.  They are capable of rendering HTML on both the client and the server.  This boosts the performance of your initial content load, and improves SEO by enabling web crawlers to easily crawl the contents of the rendered HTML, which has traditionally been a challenge with AJAX-loaded content in client-side Backbone applications.

`Rendr.View` also hides a lot of the inner workings.  Simply invoke the [render](#render) method of a view and it will re-render the template with the current state of the data.  You can also write code in the [preRender](#preRender) and [postRender](#postRender) hooks provided.

Another performance boost comes with 'lazy-loading' views (see [fetchLazy](#fetchLazy)).  When you lazy-load a view, it will wait to fetch its data from the API until the page has finished loading on the client.  After fetching the data, it will automatically render that component.  The views that don't affect SEO or are secondary to data are prime views to lazy-load.

{% include pageDoc.html name="view" %}


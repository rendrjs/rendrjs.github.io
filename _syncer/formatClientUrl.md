---
header: formatClientUrl
example: Model.formatClientUrl(url, api)
---

This function will create the URL that is expected on the client application. It requires the URL and the api (which defaults to '/api').  This will then create the URL for the [API proxy](/api-proxy).  Generally, `formatClientUrl` only needs to be invoked by `getUrl`.


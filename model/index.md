---
layout: content
title: "Model - RendrJS"
---

# Model

Rendr models are extenions on [Backbone Models](http://backbonejs.org#Model).  They are configured to run on the client and server, however some of the funcitonality works a little different between the two.  Ideally in a project you don't need to worry about these changes, but here's some documentation on how they function and some of the differences between the two states that they'll be running in.


### constructor <span>new Model([attributes], [options])</span>
<hr />

The **constructor** will create an instance of a Rendr Model.  The options are expecting a reference to the app object, this is used to hook into the sync functionality.  The constructor also invokes the parent Backbone initialization, and finally stores the instance in the model store.


### jsonKey <span>Model.jsonKey</span>
<hr />

**jsonKey** is the JSON root of the response from the API. This will automatically [parse](#parse) an API response with a root key.

```js
Model.jsonKey = 'user';

// expected data format from the API
// this will then be parsed and set onto the model
{
  user: {
    id: 1,
    name: 'Tester'
  }
}
```


### parse <span>Model.parse(response, [options])</span>
<hr />

**parse** is called when data is returned from a [fetch](http://backbonejs.org#Model-fetch) request.  The *response* is a json object, and the value returned from this function will be set as the attributes of the model.  If your API is returning a root object in the key, you can set the [jsonKey](#jsonkey) to return the attributes, withouth having to override the default functionality.



### store <span>Model.store()</span>
<hr />

This will save the data to the model store.  This data is retrieved when the veiws are being constructed.  This saves on requests as well, as the fetch function will check the store before creating the AJAX request to the server.  Store also has a default trigger setup on the `change` event of the `idAttribute`.  This means, if you modify the ID it will re-store the data.  Since the store is referencing the instance of the model, you *don't* need to setup a change event on the entire model, as it will get those changes automatically.


### url <span>Model.url or Model.url()</span>
<hr />

This has the same functionality as the [Backbone property](http://backbonejs.org#Model-url) with the add ability of passing a string with interpolation. For example: `'/model/:someAttribute'`.


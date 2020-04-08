ember-title
==============================================================================

Makes managing `document.title` in an Ember application trivial.

Compatibility
------------------------------------------------------------------------------

* Ember.js v3.12 or above
* Ember CLI v3.12 or above
* Node.js v10 or above


Installation
------------------------------------------------------------------------------

```
ember install ember-title
```


Usage
------------------------------------------------------------------------------

Applications can choose to set their title in their templates (via the
`{{title}}` helper), or in routes (by setting a `title` property). These titles
are gathered from both the route and template and combined into the final title
to be displayed.

Basic features are:

* Combining title from each "layer"
* Specify custom separator (e.g. `Foo | Bar` vs `Foo > Bar`)
* Provide a replacement instead of concatenating
* Specify the ordering (leaf -> root, or root -> leaf)


### Route Based Title

In your route files you can set the `title` property to a string:

```
export default class extends Route {
  title = "My Awesome Page";
}
```

### Template Based Title

In your template (any template!) you can invoke the `{{title}}` helper:

```hbs
{{title "My Awesome Page"}}

{{outlet}}
```

Contributing
------------------------------------------------------------------------------

See the [Contributing](CONTRIBUTING.md) guide for details.


License
------------------------------------------------------------------------------

This project is licensed under the [MIT License](LICENSE.md).

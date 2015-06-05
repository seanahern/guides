Use the `{{action}}` helper to attach a handler on a component to an event triggered on an element.

To attach an element's `click` event to the `edit()` handler of the current component:

```handlebars
<a href="#" {{action 'edit' on="click"}}>Edit</a>
```

Because the default event is `click`, this could be written more concisely as:

```handlebars
<a href="#" {{action 'edit'}}>Edit</a>
```

Any of the templates discussed above will produce an HTML element like this:

```html
<a href="#" data-ember-action="3">Edit</a>
```

Ember will delegate the event you specified to your target view's handler based upon the internally assigned `data-ember-action` id.

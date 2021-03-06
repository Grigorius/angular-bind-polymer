angular-bind-polymer
====================

Angular directive for *double* variable binding of Polymer attributes.

Installation
------------

Usage
-----

Source the directive per normal:

```html
    <script src="bower_components/angular-bind-polymer/angular_bind_polymer.js"></script>
```

Add `gr.polymerBind` as dependency for your Angular application:

```javascript
var PizzaStoreApp = angular.module('pizzaStoreApp', [
  'gr.polymerBind'
]);
```

Apply the `bind-polymer-input` directive to your custom input elements:

```html
<core-input placeholder="Placeholder text here" bind-polymer-input="testing"></core-input>
<pre>{{testing}}</pre>
```

Changes from the `<x-pizza>` custom element will now update the `pizzaState` variable in local scope.

_Note:_ changes in Angular's scope are already bound. That is, changes to `pizzaState` will update the `<x-pizza>` custom element without this or any other modules. This directive is soley used to watch for changes in custom elements for the purposes of updating a bound variable in Angular's scope.

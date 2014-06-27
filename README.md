angular-bowser
====================

This is a simple [AngularJS](http://angularjs.org/) service to provide browser and browser information.
It's heavily based on [bowser](https://github.com/ded/bowser) code.

### Dependencies

None except for AngularJS.

### Install

`bower install angular-bowser`

### Usage

Include src/angular-bowser.js in your html.

```html
<script src="bower_components/angular-pnotify/src/angular-pnotify.js"></script>
```

Add the angular-bowser module as a dependency to your application module:

```javascript
angular.module('MyApp', ['jlareau.bowser']);
```

Inject the service where you need it. A good place is in the run section of your application.

```javascript
angular.module('MyApp')
  .run(['bowser', function(bowser) {
    
    if ( bowser.msie && bowser.version <= 6 ) {
      alert('Seriously?!');
    }
    
  }]);
```

### Properties

Example of properties are: firefox, chrome, msie, opera, android, ios, safari

The browser version is always in the version property.

For more information, please check [bowser](https://github.com/ded/bowser).

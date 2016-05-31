angular-bowser
====================

This is a simple [AngularJS](http://angularjs.org/) service to provide browser information.
It's heavily based on [bowser](https://github.com/ded/bowser) code.

### Dependencies

None except for AngularJS.

### Install

`bower install --save angular-bowser`

OR 

`npm install --save angular-bowser`

### Usage

Include src/angular-bowser.js in your html.

```html
<script src="node_modules/angular-bowser/src/angular-bowser.js"></script>
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
        
            alert(`${bowser.name}, Seriously?!`);
            
        }
    
    }]);
```

### Properties

Example of properties are: firefox, chrome, msie, opera, android, ios, safari

The browser version is always in the version property.

For more information, please check [bowser](https://github.com/ded/bowser).

### See also

[ng-device-detector](https://github.com/srfrnk/ng-device-detector)

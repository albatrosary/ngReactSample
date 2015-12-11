# ngReactSample

```bash
npm init -y
npm i angular --save
npm i react --save
npm i react-dom --save
npm i ngreact --save
```

Defualt HTML:
```html
<!doctype html>
<html>
  <head>
    <title>angular-react hello example</title>
  </head>
  <body ng-app="app" ng-controller="mainCtrl">
  </body>
</html>
```

Call JavaScript:
```html
<script src="node_modules/angular/angular.js"></script>
<script src="node_modules/react/dist/react.js"></script>
<script src="node_modules/react-dom/dist/react-dom.js"></script>
<script src="node_modules/ngreact/ngReact.js"></script>
<script src="app.js"></script>
```

Angular Controller, value, directive:
```javascript
var app = angular.module('app', ['react']);

app.controller('mainCtrl', function( $scope) {
});

var Hello = React.createClass({});

app.value("Hello", Hello);

app.directive('hello', function(reactDirective) {
  return reactDirective(Hello);
});
```

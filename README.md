# PolymerElectronAppBehavior

See https://github.com/csakaszamok/electron-polymerapp-demo for demo.

##use
- Change urls in the index.html:  
old:  
```html
<link rel="shortcut icon" sizes="32x32" href="/images/app-icon-32.png">
<link rel="manifest" href="/manifest.json">
<link rel="import" href="/src/my-app.html">
``` 
```js
navigator.serviceWorker.register('/service-worker.js');
```
new:  
```html
<link rel="shortcut icon" sizes="32x32" href="./images/app-icon-32.png">
<link rel="manifest" href="./manifest.json">
<link rel="import" href="./src/my-app.html">
``` 
```js
navigator.serviceWorker.register('./service-worker.js');
```

- Install bower component:

```
bower install PolymerElectronAppBehavior
```

- Add link to the polymer app:
```html
...
<link rel="import" href="my-icons.html">
<link rel="import" href="../bower_components/PolymerElectronAppBehavior/electronapp-behavior.html">
<dom-module id="my-app">
...
```

- Add behavior to the behaviors:

```js
...
is: 'my-app',
      behaviors: [ElectronAppBehavior],
      properties: {
...      
```

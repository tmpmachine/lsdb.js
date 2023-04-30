# lsdb.js
Plain JS local storage utility/helper for storing application config in the form of object.

## Installation (CDN jsDelivr)
Include in your application :
```html
<script src="https://cdn.jsdelivr.net/gh/tmpmachine/lsdb.js@v1.0.0/lsdb.js"></script>
```
```
https://cdn.jsdelivr.net/gh/tmpmachine/lsdb.js@v1.0.0/lsdb.js
```
or use minified version :
```html
<script src="https://cdn.jsdelivr.net/gh/tmpmachine/lsdb.js@v1.0.0/lsdb.min.js"></script>
```
```
https://cdn.jsdelivr.net/gh/tmpmachine/lsdb.js@v1.0.0/lsdb.min.js
```

## Usage Example
```js
let storageName = 'appdata-NzkwMTI0NA';

// init and load data from storage
window.lsdb = new Lsdb(storageName, {
  root: {
    stringData: '',
    numberData: -1,
    dynamicData: {},
  },
});

function storeLsdb() {
  window.lsdb.save();
}

function resetLsdb() {
  window.lsdb.reset();
}
```

Accessing and storing the data :
```js
// access
console.log(window.lsdb.data.stringData)

// store, only temporary until save() is called.
window.lsdb.data.stringData = 'John Doe';
```


# Latinize.js

Simple library to convert accents (diacritics) from strings to latin characters.

FORK from unmaintained https://github.com/dundalek/latinize

## Install

```
npm install latinize-to-ascii
```

## Usage

node.js / CommonJS

```javascript
var latinize = require('latinize');
latinize('ỆᶍǍᶆṔƚÉ áéíóúýčďěňřšťžů'); // => 'ExAmPlE aeiouycdenrstzu'
```

AMD

```javascript
require(['latinize'], function(latinize){
  latinize('ỆᶍǍᶆṔƚÉ áéíóúýčďěňřšťžů');
});
```

browser

```html
<script src="dist/latinize.min.js"></script>
<script>
    document.write(latinize('ỆᶍǍᶆṔƚÉ áéíóúýčďěňřšťžů'));
</script>
```

ESM / MJS / ES6+ / Javascript Module

```javascript
import latinize from 'dist/latinize.mjs';
latinize('ỆᶍǍᶆṔƚÉ áéíóúýčďěňřšťžů'); // => 'ExAmPlE aeiouycdenrstzu'
```


You can use the `latinize.characters` object to access the translation table or to change the mapping:

```javascript
latinize.characters['Ω'] = 'O';

// modify the behavior for German umlauts
_.extend(latinize.characters,
  {'Ä': 'Ae', 'Ä': 'Ae', 'Ü': 'Ue', 'ä': 'ae', 'ö': 'oe', 'ü': 'ue'});
```

## Details

Is is a lookup table taken from [http://jsperf.com/latinize](http://jsperf.com/latinize) packaged for node and browser. Visit the link to see more approaches.

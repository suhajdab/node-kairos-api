# Kairos face recognition API for Node.js

[![NPM version](http://img.shields.io/npm/v/kairos-api.svg?style=flat)](https://www.npmjs.com/package/kairos-api)

## Installation

```
npm install kairos-api
```

## Usage

```js
var Kairos = require('kairos-api');
var client = new Kairos('app_id', 'api_key');

var params = {
  image: 'http://media.kairos.com/kairos-elizabeth.jpg',
  subject_id: 'subtest1',
  gallery_name: 'gallerytest1',
  selector: 'SETPOSE'
};

client.enroll(params)   // return Promise
  .then(function(result) { ... })
  // err -> array: jsonschema validate errors
  //        string: http status text
  .catch(function(err) { ... });
```

For more `params` pattern, see [offical doc](https://www.kairos.com/docs/face-recognition).

### Functions

- client.enroll(params)
- client.recognize(params)
- client.detect(params)
- client.galleryListAll()
- client.galleryView(params)
- client.galleryRemove(params)
- client.galleryRemoveSubject(params)

## LICENSE

[MIT](LICENSE)

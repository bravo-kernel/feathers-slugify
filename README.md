# feathers-slugify

[![Build Status](https://travis-ci.org/https://github.com/Mattchewone/feathers-slugify.git.png?branch=master)](https://travis-ci.org/https://github.com/Mattchewone/feathers-slugify.git)
[![Code Climate](https://codeclimate.com/github/https://github.com/Mattchewone/feathers-slugify.git/badges/gpa.svg)](https://codeclimate.com/github/https://github.com/Mattchewone/feathers-slugify.git)
[![Test Coverage](https://codeclimate.com/github/https://github.com/Mattchewone/feathers-slugify.git/badges/coverage.svg)](https://codeclimate.com/github/https://github.com/Mattchewone/feathers-slugify.git/coverage)
[![Dependency Status](https://img.shields.io/david/https://github.com/Mattchewone/feathers-slugify.git.svg?style=flat-square)](https://david-dm.org/https://github.com/Mattchewone/feathers-slugify.git)
[![Download Status](https://img.shields.io/npm/dm/feathers-slugify.svg?style=flat-square)](https://www.npmjs.com/package/feathers-slugify)

> Feathers hook to slugify properties

## Installation

```
npm install feathers-slugify --save
```

## Documentation

Please refer to the [feathers-slugify documentation](http://docs.feathersjs.com/) for more details.

## Complete Example

Here's an example of a Feathers server that uses `feathers-slugify`. 

```js
const feathers = require('feathers');
const rest = require('feathers-rest');
const hooks = require('feathers-hooks');
const bodyParser = require('body-parser');
const errorHandler = require('feathers-errors/handler');
const plugin = require('feathers-slugify');

// Initialize the application
const app = feathers()
  .configure(rest())
  .configure(hooks())
  // Needed for parsing bodies (login)
  .use(bodyParser.json())
  .use(bodyParser.urlencoded({ extended: true }))
  // Initialize your feathers plugin
  .use('/plugin', plugin())
  .use(errorHandler());

app.listen(3030);

console.log('Feathers app started on 127.0.0.1:3030');
```

## License

Copyright (c) 2017

Licensed under the [MIT license](LICENSE).
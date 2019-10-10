# processing-context

[![npm version](https://badge.fury.io/js/processing-context.svg)](https://www.npmjs.com/package/processing-context)
[![npm downloads](https://img.shields.io/npm/dt/processing-context.svg)](https://www.npmjs.com/package/processing-context)
[![dependencies](https://img.shields.io/david/litichevskiydv/processing-context.svg)](https://www.npmjs.com/package/processing-context)
[![dev dependencies](https://img.shields.io/david/dev/litichevskiydv/processing-context.svg)](https://www.npmjs.com/package/processing-context)
[![Build Status](https://travis-ci.org/litichevskiydv/processing-context.svg?branch=master)](https://travis-ci.org/litichevskiydv/processing-context)
[![Coverage Status](https://coveralls.io/repos/github/litichevskiydv/processing-context/badge.svg?branch=master)](https://coveralls.io/github/litichevskiydv/processing-context?branch=master)

Globally accessible processing context based on async_hooks

# Install

`npm i processing-context`

# Usage

```javascript
const processingContext = require("processing-context");
const defaultContext = processingContext.defaultContext;

/*...*/

const key = "counter";
const initialValue = 3;

/*...*/

processingContext.create().set(key, initialValue);
const updatedValue = await new Promise(resolve => resolve(defaultContext.get(key) + 2));
```

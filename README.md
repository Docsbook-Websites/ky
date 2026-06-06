# ky

[![npm version](https://img.shields.io/npm/v/ky.svg)](https://www.npmjs.com/package/ky)
[![Build Status](https://travis-ci.com/sindresorhus/ky.svg?branch=master)](https://travis-ci.com/sindresorhus/ky)
[![Coverage Status](https://coveralls.io/repos/github/sindresorhus/ky/badge.svg?branch=master)](https://coveralls.io/github/sindresorhus/ky?branch=master)

> Simplified HTTP requests

## Install

```bash
npm install ky
```

## Usage

### Basic Usage

```javascript
import ky from 'ky';

const response = await ky('https://api.example.com', { method: 'GET' });
const data = await response.json();
console.log(data);
```

### Custom Options

You can customize your request using options:

```javascript
const response = await ky('https://api.example.com', {
  method: 'POST',
  json: {
    key: 'value'
  },
});
```

### Catching Errors

You can catch errors using try-catch:

```javascript
try {
  const response = await ky('https://api.example.com');
} catch (error) {
  console.error(error);
}
```

## API

### ky(url, options)

- **url:** The URL to which the request is sent.
- **options:** An object containing options for the request.

## License

MIT License.
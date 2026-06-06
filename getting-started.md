# Getting Started with ky

`ky` is a versatile HTTP client that simplifies making requests. This guide will help you get started with using `ky` in your project.

## Installation
To use `ky`, you need to install it via npm:

```bash
npm install ky
```

## Basic Example
Here is a simple example to fetch data from an API:

```javascript
import ky from 'ky';

async function fetchData() {
    const response = await ky('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
}

fetchData();
```

## Customizing Requests
You can customize the request with various options like method, headers, body, etc. For example:

```javascript
await ky('https://api.example.com/data', {
  method: 'POST',
  json: { key: 'value' },
  headers: { 'Authorization': 'Bearer token' }
});
```

## Handling Errors
Use a try-catch block to handle errors while making requests:

```javascript
try {
    await ky('https://api.example.com/data');
} catch (error) {
    console.error(error);
}
```

## Conclusion
You're now ready to use `ky` for your HTTP requests. For more advanced usage, refer to the [API documentation](https://github.com/sindresorhus/ky).


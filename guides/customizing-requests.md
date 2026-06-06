# Customizing Requests in ky

`ky` allows you to customize HTTP requests in various ways. This guide outlines how to modify requests with headers, body, and more.

## Custom Headers
To add custom headers to your request, use the `headers` option:

```javascript
await ky('https://api.example.com/data', {
    headers: {
        'Authorization': 'Bearer token',
        'Content-Type': 'application/json',
    },
});
```

## JSON Body
To send JSON data in a POST request, you can use the `json` option:

```javascript
await ky('https://api.example.com/data', {
    method: 'POST',
    json: {
        key: 'value'
    },
});
```

## Timeout
To set a timeout for your requests, use the `timeout` option:

```javascript
await ky('https://api.example.com/data', {
    timeout: 10000, // 10 seconds
});
```

## Conclusion
Customizing requests in `ky` allows for versatile and flexible API interactions. Use the various options available to suit your needs.

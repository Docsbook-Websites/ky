# Advanced Usage of ky

This guide covers some advanced features and patterns when using `ky` for HTTP requests.

## Streaming Requests
`ky` supports streaming responses, allowing you to read data as it arrives:

```javascript
const response = await ky('https://api.example.com/large-data');
const reader = response.body.getReader();

const decoder = new TextDecoder();
let done = false;
while (!done) {
    const {value, done: readerDone} = await reader.read();
    done = readerDone;
    console.log(decoder.decode(value));
}
```

## Retry Feature
To automatically retry failed requests, you can use the `retry` option:

```javascript
await ky('https://api.example.com/data', {
    retry: {
        limit: 3,
    },
});
```

## Conclusion
Using advanced features in `ky`, you can optimize and enhance your HTTP request handling. Explore various options to fit your application’s needs.

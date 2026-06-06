# Error Handling in ky

`ky` provides a simple way to handle errors when making HTTP requests. This guide explains common error handling patterns.

## Basic Try-Catch
The simplest way to catch errors is by using a try-catch block:

```javascript
try {
    const response = await ky('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
} catch (error) {
    console.error(error);
}
```

## Custom Error Types
`ky` throws errors with specific names based on the HTTP response. You can check the error type like this:

```javascript
try {
    await ky('https://api.example.com/data');
} catch (error) {
    if (error.name === 'HTTPError') {
        console.error('HTTP error:', error);
    } else {
        console.error('Unexpected error:', error);
    }
}
```

## Conclusion
Proper error handling is vital for robust applications. Use try-catch for simpler scenarios and check error types for more detailed handling.

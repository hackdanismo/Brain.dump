# Axios

To install `Axios`:

```shell
$ npm install axios
```

A `HEAD` request is like a `GET` request, but the server doesn't return the response body — only the headers. It is mainly used to:

+ Check if resources exist.
+ Get `metadata` like: `Content-Type`, `Content-Length`, or `Last-Modified` without downloading the full content of the page.
+ Test API endpoints or caching behaviour. 

The Axios `head()` syntax:

```javascript
axios.head(url[, config])
```

+ `url`: The endpoint to be queried.
+ `config`: (optional) Request configuration object (headers, params, etc.).

Example:

```javascript
// This is using CommonJS to import the Axios library, but we can use import when using modules
const axios = require('axios');

// Define an asynchronous function that checks a URL endpoint
async function checkFile() {
    try {
        // Send an HTTP HEAD request to the URL endpoint specified using the head() method of Axios
        const response = await axios.head('https://example.com/image.jpg);
        console.log('Headers:', response.headers);
        console.log('Status:', response.status);
    } catch (error) {
        console.error('Error:', error.message);
    }
}

// Call the function to execute the code
checkFile();
```

The `response.status` will return the `HTTP status` from the request e.g. `200`, `404` etc.

The output might look like this:

```shell
Headers: {
    'content-type': 'image/jpeg',
    'content-length': '2048',
    'last-modified': 'Thur, 30 Oct 2025 10:00:00 GMT'
}
Status: 200
```

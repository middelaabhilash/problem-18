# Express Request Logging Middleware

## Problem

Create an Express middleware function that logs the HTTP method and URL path of
each request, then make sure the `GET /` route passes through that middleware
before sending its response.

## Expected behavior

When a client sends a `GET` request to `/`:

1. The middleware logs the request method (`GET`) and path (`/`) to the
   server's console.
2. The route responds with the text `Coding Ninjas!`.

The middleware must call `next()` so the request continues to the route
handler.

## Run locally

Install the dependencies and start the server:

```sh
npm install
node server.js
```

The server listens on port `5000`. Visit <http://localhost:5000/> or send a
request with:

```sh
curl http://localhost:5000/
```

The response body should be:

```text
Coding Ninjas!
```

The server console should show the method and path:

```text
GET
/
```

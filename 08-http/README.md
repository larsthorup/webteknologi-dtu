# HTTP - front-end web technology - 2023-03-20

Fetch and send data between the browser and servers

Please read:

- [Identifying resources on the Web](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/Identifying_resources_on_the_Web)
- [An overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)
- [HTTP Messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)
- [HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)
- [HTTP response status codes](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
- [Synchronizing with Effects](https://beta.reactjs.org/learn/synchronizing-with-effects)

## Why is HTTP exciting?

- Text-based protocol used almost everywhere, easy to debug
- Single request / response, stateless, thus very reliable

## URLs

- scheme: http / https
- host / authority
- port, default based on scheme: 80 / 443
- path
- query
- hash / fragment, not sent!

## HTTP messages

- Request Start line: method, URL, version
- Response status line: version, status code, status text
- Headers
- Body

## HTTP request methods

- POST - create
- GET - read, cachable
- PUT - update, idempotent
- DELETE - delete, idempotent
- PATCH - partial update, not idempotent

## HTTP from JavaScript

- fetch
- response: ok, status, statusText, json
- url encoding, URL, URLSearchParams
- JSON serialization: parse(), stringify()
- Base64 (ASCII) encoding for binary data: btoa(), atob()

## HTTP from React

- event handler
- useEffect, dependencies, cleanup
- loading indicators
- error reporting
- browser caching, app caching, cache invalidation

## HTTP type safety

- manual type definition
- OpenAPI, type generation
- run-time type validation

## Testing HTTP requests

- mock fetch
- simulating errors

## Debugging

- Browser Developer Tools
- requestbin.com

## Next time

[Security](..).

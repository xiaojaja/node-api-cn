<!-- YAML
added: v8.4.0
-->

* {string}

Request URL string. This contains only the URL that is present in the actual
HTTP request. If the request is:

```http
GET /status?name=ryan HTTP/1.1
Accept: text/plain
```

Then `request.url` will be:

<!-- eslint-disable semi -->
```js
'/status?name=ryan'
```

To parse the url into its parts, `require('url').parse(request.url)`
can be used:

```console
$ node
> require('url').parse('/status?name=ryan')
Url {
  protocol: null,
  slashes: null,
  auth: null,
  host: null,
  port: null,
  hostname: null,
  hash: null,
  search: '?name=ryan',
  query: 'name=ryan',
  pathname: '/status',
  path: '/status?name=ryan',
  href: '/status?name=ryan' }
```

To extract the parameters from the query string, the
`require('querystring').parse` function can be used, or
`true` can be passed as the second argument to `require('url').parse`.

```console
$ node
> require('url').parse('/status?name=ryan', true)
Url {
  protocol: null,
  slashes: null,
  auth: null,
  host: null,
  port: null,
  hostname: null,
  hash: null,
  search: '?name=ryan',
  query: { name: 'ryan' },
  pathname: '/status',
  path: '/status?name=ryan',
  href: '/status?name=ryan' }
```


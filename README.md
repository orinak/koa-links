# koa-links

Use `ctx.links` as proxy to `ctx.response.headers['Link']` in [Koa][koa] apps

[koa]: https://github.com/koajs/koa


## Usage

```js
const Koa = require('koa')
const links = require('koa-links')

const app = new Koa()

app.use(links())

app.use(ctx => {
  ctx.links.self = 'http://example.com/'
  ctx.body = 'done'
})
```

## Installation

Install using npm

```sh
npm install koa-links
```

## License

MIT

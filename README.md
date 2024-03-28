# `cloudflare-d1`

Create D1 and copy output to the `wrangler.toml`:

```shell
wrangler d1 create cloudflare-d1-tutorial
```

Create migrations folder `migrations` and create a new migration:

```shell
wrangler d1 migrations list cloudflare-d1

wrangler d1 migrations apply cloudflare-d1
wrangler d1 migrations apply cloudflare-d1 --remote=true
```

Local database is created in the path `.wrangler/state/v3/d1/miniflare-D1DatabaseObject`, you can connect to it and also use when developing locally:

```shell
wrangler dev src/index.ts

Your worker has access to the following bindings:
- D1 Databases:
  - DB: cloudflare-d1-tutorial
```

Vitest: https://github.com/cloudflare/workers-sdk/tree/main/fixtures/vitest-pool-workers-examples/d1

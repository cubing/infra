# Cubing infra

Infrastructure info for projects associated with the following:

- [`github.com/cubing`](https://github.com/cubing)
- [`cubing.net`](https://www.cubing.net/)
- [`cubing.org` ](https://cubing.org/)

## Key

- NC — Namecheap[^1]
- DH — DreamHost[^1]
- GCE — Google (Cloud) Compute Engine [^1]
- CF — Cloudflare[^1]
- GH — GitHub (under [`github.com/cubing`](https://github.com/cubing))
- SW — offline support through service worker

[^1]: Currently `@lgarron`'s personal account.

## Sites & Apps

| Site / App                                              | Regis-tration | DNS    | Hosting                                                                                                                          | Repo                                                                          | Dev Port                                                                                                                            | Deployment                                                                                                                                                                                                                                                |
| ------------------------------------------------------- | ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`alg.cubing.net`](https://alg.cubing.net/)             | NC            | DH     | GH Pages                                                                                                                         | [`cubing/alg.cubing.net`](https://github.com/cubing/alg.cubing.net)           | N/A                                                                                                                                 | In-tree [`docs` folder](https://github.com/cubing/alg.cubing.net/tree/main/docs)                                                                                                                                                                          |
| [`cdn.cubing.net`](https://cdn.cubing.net/)             | NC            | DH     | DH + CF                                                                                                                          | [`cubing/cdn.cubing.net`](https://github.com/cubing/cdn.cubing.net)           | [`3336`](https://github.com/cubing/cdn.cubing.net/blob/bf81d6fb9c9338b5825b7a586a1418c6bbf77ce9/script/dev.Caddyfile#L1)            | [`rsync`](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L57-L67) (`cubing_deploy@`) + [CF API](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L83-L87) |
| [`icons.cubing.net`](https://icons.cubing.net/)         | NC            | DH     | GH Pages                                                                                                                         | [`cubing/icons`](https://github.com/cubing/icons)                             | N/A                                                                                                                                 | [GH Actions](https://github.com/cubing/icons/blob/022972632477498c2624b084bf303598596df8e4/.github/workflows/deploy.yml)                                                                                                                                  |
| [`js.cubing.net`](https://js.cubing.net/)               | NC            | DH     | GH Pages                                                                                                                         | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [`3333`](https://github.com/lgarron/backup-cubing.js/blob/2ab56c7cb192f9a07d4cc12f2ad240421160a804/script/build/targets.js#L77)[^4] | [GH Actions](https://github.com/cubing/cubing.js/blob/main/.github/workflows/pages.yml)                                                                                                                                                                   |
| [`scramble.cubing.net`](https://scramble.cubing.net/)   | NC            | DH     | DH + SW                                                                                                                          | [`cubing/scramble.cubing.net`](https://github.com/cubing/scramble.cubing.net) | [`3335`](https://github.com/cubing/scramble.cubing.net/blob/f82266b48446d56f7af24042fbe61ab530adfa44/package.json#L26)              | [`rsync`](https://github.com/cubing/scramble.cubing.net/blob/e7d2d36c885b8f938fd4eff4ac3911cf523bb26c/Makefile#L19-L30) (`lgarron@`)                                                                                                                      |
| [`timer.cubing.net`](https://timer.cubing.net/)         | NC            | DH     | DH + SW                                                                                                                          | [`cubing/timer`](https://github.com/cubing/timer)                             | [`3334`](https://github.com/cubing/timer/blob/5489b82b017a2c2e82211875af2004bfcb7c4a34/script/dev.js#L6)                            | [`rsync`](https://github.com/cubing/timer/blob/5489b82b017a2c2e82211875af2004bfcb7c4a34/Makefile#L17-L27) (`lgarron@`)                                                                                                                                    |
| [`alpha.twizzle.net`](https://alpha.twizzle.net/)       | NC            | DH     | DH                                                                                                                               | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [`3333`](https://github.com/lgarron/backup-cubing.js/blob/2ab56c7cb192f9a07d4cc12f2ad240421160a804/script/build/targets.js#L77)[^4] | [`rsync`](https://github.com/lgarron/backup-cubing.js/blob/75a59447c085dbe4275ee0c8ebfb21852a5adb40/script/deploy/twizzle.js) (`cubing_deploy@`)                                                                                                          |
| [`api.twizzle.net`](https://api.twizzle.net/)[^2]       | NC            | DH[^3] | [GCE](https://console.cloud.google.com/compute/instancesDetail/zones/us-west2-b/instances/api-twizzle-net?project=cubing) + Deno | [`cubing/api.twizzle.net`](https://github.com/cubing/api.twizzle.net)         | N/A                                                                                                                                 | [`gcloud compute scp`](https://github.com/cubing/api.twizzle.net/blob/def81359cb27a49d0b40ffbf60b08df7d046b386/Makefile#L19-L30)                                                                                                                          |
| [`archive.cubing.net`](https://archive.cubing.net/) | NC | DH | GH Pages | [`cubing/archive.cubing.net`](https://github.com/cubing/archive.cubing.net) | N/A | In-tree root folder |
| [`standards.cubing.net`](https://standards.cubing.net/) | NC | DH | GH Pages | [`cubing/standards`](https://github.com/cubing/standards) | N/A | In-tree root folder |
| [`qqtimer.net`](https://qqtimer.net/) | NC | DH | GH Pages | [`cubing/qqTimer`](https://github.com/cubing/qqTimer) | N/A | In-tree [`docs` folder](https://github.com/cubing/qqTimer/tree/main/docs) |
| [`cubing.org`](https://cubing.org/) | NC | DH | GH Pages | [`cubing/cubing.org`](https://github.com/cubing/cubing.org) | N/A | In-tree root folder |
| [`cubing-org.slack.com`](https://cubing-org.slack.com/) | N/A           | N/A    | Slack                                                                                                                            | N/A                                                                           | N/A                                                                                                                                 | N/A                                                                                                                                                                                                                                                       |

[^2]: Used by: <https://twizzle.net/stream>
[^3]: A record: `35.236.43.166`
[^4]: Shared

## Organizations

### GitHub

- URL: https://github.com/cubing
- Org settings URL: https://github.com/organizations/cubing/settings/profile
- 2FA enforcement for members: No (TODO)
- Owners: `@lgarron`, `@jfly`

Certain repos have elevated privileges for maintainers. (TODO: document these.)

### `npm`

- URL: https://www.npmjs.com/org/cubing
- Org settings URL: https://www.npmjs.com/settings/cubing/packages
- 2FA enforcement for members: No (TODO)
- Admins: `@lgarron` (TODO)

## Conventions

- We generally publishe code under one of the following licenses:
  - Dedicate to the public domain using the [Unliense](https://unlicense.org/).
  - MPL: for projects we want to encourage open collaboration for.
  - MIT: for projects with permissive usage.
  - GPL: Do not use for new projects. Use the MPL instead.
- Makefile conventions: <https://github.com/lgarron/Makefile-convention>, particularly: `make dev` and `make build`
- JS projects:
  - Language: TypeScript
  - Bundler: `esbuild`
  - Formatter: `rome`

Many of these conventions are available in: <https://github.com/lgarron/ts-project-template>

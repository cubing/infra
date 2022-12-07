# Cubing infra

Infrastructure info for `cubing.net` / `cubing.org` / `github.com/cubing` projects.

## Key

- NC — Namecheap[^1]
- DH — DreamHost[^1]
- GCE — Google (Cloud) Compute Engine [^1]
- CF — Cloudflare[^1]
- GH — GitHub (under [`github.com/cubing`](https://github.com/cubing))
- SW — offline support through service worker

[^1]: Currently `@lgarron`'s personal account.

## Sites & Apps

| Site / App                                              | Regis-tration | DNS    | Hosting                                                                                                                          | Repo                                                                          | Deployment                                                                                                                                                                                                                                                |
| ------------------------------------------------------- | ------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`alg.cubing.net`](https://alg.cubing.net/)             | NC            | DH     | GH Pages                                                                                                                         | [`cubing/alg.cubing.net`](https://github.com/cubing/alg.cubing.net)           | In-tree [`docs` folder](https://github.com/cubing/alg.cubing.net/tree/main/docs)                                                                                                                                                                          |
| [`cdn.cubing.net`](https://cdn.cubing.net/)             | NC            | DH     | DH + CF                                                                                                                          | [`cubing/cdn.cubing.net`](https://github.com/cubing/cdn.cubing.net)           | [`rsync`](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L57-L67) (`cubing_deploy@`) + [CF API](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L83-L87) |
| [`icons.cubing.net`](https://icons.cubing.net/)         | NC            | DH     | GH Pages                                                                                                                         | [`cubing/icons`](https://github.com/cubing/icons)                             | [GH Actions](https://github.com/cubing/icons/blob/022972632477498c2624b084bf303598596df8e4/.github/workflows/deploy.yml)                                                                                                                                  |
| [`js.cubing.net`](https://js.cubing.net/)               | NC            | DH     | GH Pages                                                                                                                         | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [GH Actions](https://github.com/cubing/cubing.js/blob/main/.github/workflows/pages.yml)                                                                                                                                                                   |
| [`scramble.cubing.net`](https://scramble.cubing.net/)   | NC            | DH     | DH + SW                                                                                                                          | [`cubing/scramble.cubing.net`](https://github.com/cubing/scramble.cubing.net) | [`rsync`](https://github.com/cubing/scramble.cubing.net/blob/e7d2d36c885b8f938fd4eff4ac3911cf523bb26c/Makefile#L19-L30) (`lgarron@`)                                                                                                                      |
| [`timer.cubing.net`](https://timer.cubing.net/)         | NC            | DH     | DH + SW                                                                                                                          | [`cubing/timer`](https://github.com/cubing/timer)                             | [`rsync`](https://github.com/cubing/timer/blob/5489b82b017a2c2e82211875af2004bfcb7c4a34/Makefile#L17-L27) (`lgarron@`)                                                                                                                                    |
| [`alpha.twizzle.net`](https://alpha.twizzle.net/)       | NC            | DH     | DH                                                                                                                               | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [`rsync`](https://github.com/lgarron/backup-cubing.js/blob/75a59447c085dbe4275ee0c8ebfb21852a5adb40/script/deploy/twizzle.js) (`cubing_deploy@`)                                                                                                          |
| [`api.twizzle.net`](https://api.twizzle.net/)[^2]           | NC            | DH[^3] | [GCE](https://console.cloud.google.com/compute/instancesDetail/zones/us-west2-b/instances/api-twizzle-net?project=cubing) + Deno | [`cubing/api.twizzle.net`](https://github.com/cubing/api.twizzle.net)         | [`gcloud compute scp`](https://github.com/cubing/api.twizzle.net/blob/def81359cb27a49d0b40ffbf60b08df7d046b386/Makefile#L19-L30)                                                                                                                          |
| [`cubing-org.slack.com`](https://cubing-org.slack.com/) | N/A           | N/A    | Slack                                                                                                                            | N/A                                                                           | N/A                                                                                                                                                                                                                                                       |

[^2]: Used by: <https://twizzle.net/stream>
[^3]: A record: `35.236.43.166`

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

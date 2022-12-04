# Cubing infra

Infrastructure info for `cubing.net` / `cubing.org` / `github.com/cubing` projects.

## Key

- NC — Namecheap[^1]
- DH — DreamHost[^1]
- CF — Cloudflare[^1]
- GH — GitHub (under [`github.com/cubing`](https://github.com/cubing))

## Sites

| Site                                                    | Regis-tration | DNS | Hosting  | Repo                                                                | Deployment                                                                                                                                                                                                                                                |
| ------------------------------------------------------- | ------------- | --- | -------- | ------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`alg.cubing.net`](https://alg.cubing.net/)             | NC            | DH  | GH Pages | [`cubing/alg.cubing.net`](https://github.com/cubing/alg.cubing.net) | In-tree [`docs` folder](https://github.com/cubing/alg.cubing.net/tree/main/docs)                                                                                                                                                                          |
| [`cdn.cubing.net`](https://cdn.cubing.net/)             | NC            | DH  | DH + CF  | [`cubing/cdn.cubing.net`](https://github.com/cubing/cdn.cubing.net) | [`rsync`](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L57-L67) (`cubing_deploy@`) + [CF API](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L83-L87) |
| [`js.cubing.net`](https://js.cubing.net/)               | NC            | DH  | GH Pages | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)           | [GH Actions](https://github.com/cubing/cubing.js/blob/main/.github/workflows/pages.yml)                                                                                                                                                                   |
| [`alpha.twizzle.net`](https://alpha.twizzle.net/)       | NC            | DH  | DH       | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)           | [`rsync`](https://github.com/lgarron/backup-cubing.js/blob/75a59447c085dbe4275ee0c8ebfb21852a5adb40/script/deploy/twizzle.js) (`cubing_deploy@`)                                                                                                          |
| [`cubing-org.slack.com`](https://cubing-org.slack.com/) | N/A           | N/A | Slack    | N/A                                                                 | N/A                                                                                                                                                                                                                                                       |

[^1]: Currently `@lgarron`'s personal account.

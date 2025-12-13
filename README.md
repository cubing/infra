# Cubing infra

Infrastructure info for projects associated with the following:

- [`github.com/cubing`](https://github.com/cubing)
- [`cubing.net`](https://www.cubing.net/)
- [`cubing.org`](https://cubing.org/)

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
| [`alg.cubing.net`](https://alg.cubing.net/)             | NC            | DH     | GH Pages[^5]                                                                                                                     | [`cubing/alg.cubing.net`](https://github.com/cubing/alg.cubing.net)           | N/A                                                                                                                                 | In-tree [`docs` folder](https://github.com/cubing/alg.cubing.net/tree/main/docs)                                                                                                                                                                          |
| [`cdn.cubing.net`](https://cdn.cubing.net/)             | NC            | DH     | DH + CF                                                                                                                          | [`cubing/cdn.cubing.net`](https://github.com/cubing/cdn.cubing.net)           | [`3336`](https://github.com/cubing/cdn.cubing.net/blob/bf81d6fb9c9338b5825b7a586a1418c6bbf77ce9/script/dev.Caddyfile#L1)            | [`rsync`](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L57-L67) (`cubing_deploy@`) + [CF API](https://github.com/cubing/cdn.cubing.net/blob/7eae4585d9afd9a1d0a6aa559b2c8f5d137d9dd9/Makefile#L83-L87) |
| [`icons.cubing.net`](https://icons.cubing.net/)         | NC            | DH     | GH Pages[^5]                                                                                                                     | [`cubing/icons`](https://github.com/cubing/icons)                             | N/A                                                                                                                                 | [GH Actions](https://github.com/cubing/icons/blob/022972632477498c2624b084bf303598596df8e4/.github/workflows/deploy.yml)                                                                                                                                  |
| [`js.cubing.net`](https://js.cubing.net/)               | NC            | DH     | GH Pages[^5]                                                                                                                     | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [`3333`](https://github.com/lgarron/backup-cubing.js/blob/2ab56c7cb192f9a07d4cc12f2ad240421160a804/script/build/targets.js#L77)[^4] | [GH Actions](https://github.com/cubing/cubing.js/blob/main/.github/workflows/pages.yml)                                                                                                                                                                   |
| [`scramble.cubing.net`](https://scramble.cubing.net/)   | NC            | DH     | DH + SW                                                                                                                          | [`cubing/scramble.cubing.net`](https://github.com/cubing/scramble.cubing.net) | [`3335`](https://github.com/cubing/scramble.cubing.net/blob/f82266b48446d56f7af24042fbe61ab530adfa44/package.json#L26)              | [`rsync`](https://github.com/cubing/scramble.cubing.net/blob/e7d2d36c885b8f938fd4eff4ac3911cf523bb26c/Makefile#L19-L30) (`lgarron@`)                                                                                                                      |
| [`timer.cubing.net`](https://timer.cubing.net/)         | NC            | DH     | DH + SW                                                                                                                          | [`cubing/timer`](https://github.com/cubing/timer)                             | [`3334`](https://github.com/cubing/timer/blob/5489b82b017a2c2e82211875af2004bfcb7c4a34/script/dev.js#L6)                            | [`rsync`](https://github.com/cubing/timer/blob/5489b82b017a2c2e82211875af2004bfcb7c4a34/Makefile#L17-L27) (`lgarron@`)                                                                                                                                    |
| [`alpha.twizzle.net`](https://alpha.twizzle.net/)       | NC            | DH     | DH                                                                                                                               | [`cubing/cubing.js`](https://github.com/cubing/cubing.js)                     | [`3333`](https://github.com/lgarron/backup-cubing.js/blob/2ab56c7cb192f9a07d4cc12f2ad240421160a804/script/build/targets.js#L77)[^4] | [`rsync`](https://github.com/lgarron/backup-cubing.js/blob/75a59447c085dbe4275ee0c8ebfb21852a5adb40/script/deploy/twizzle.js) (`cubing_deploy@`)                                                                                                          |
| [`api.twizzle.net`](https://api.twizzle.net/)[^2]       | NC            | DH[^3] | [GCE](https://console.cloud.google.com/compute/instancesDetail/zones/us-west2-b/instances/api-twizzle-net?project=cubing) + Deno | [`cubing/api.twizzle.net`](https://github.com/cubing/api.twizzle.net)         | [`3337`](https://github.com/cubing/api.twizzle.net/blob/9ec561872915b13a19004a3b87c013ecc8055c72/src/api.twizzle.net/server/TwizzleAPIServer.ts#L29)                                                                                                                                 | [`gcloud compute scp`](https://github.com/cubing/api.twizzle.net/blob/def81359cb27a49d0b40ffbf60b08df7d046b386/Makefile#L19-L30)                                                                                                                          |
| [`archive.cubing.net`](https://archive.cubing.net/) | NC | DH | GH Pages[^5] | [`cubing/archive.cubing.net`](https://github.com/cubing/archive.cubing.net) | N/A | In-tree root folder |
| [`standards.cubing.net`](https://standards.cubing.net/) | NC | DH | GH Pages[^5] | [`cubing/standards`](https://github.com/cubing/standards) | N/A | In-tree root folder |
| [`qqtimer.net`](https://qqtimer.net/) | NC | [NC](https://ap.www.namecheap.com/Domains/DomainControlPanel/qqtimer.net/advancedns) | GH Pages | [`cubing/qqTimer`](https://github.com/cubing/qqTimer) | N/A | In-tree [`docs` folder](https://github.com/cubing/qqTimer/tree/main/docs) |
| [`cubing.org`](https://cubing.org/) | NC | NC | GH Pages | [`cubing/cubing.org`](https://github.com/cubing/cubing.org) | N/A | In-tree root folder |
| [`cubing-org.slack.com`](https://cubing-org.slack.com/) | N/A           | N/A    | Slack                                                                                                                            | N/A                                                                           | N/A                                                                                                                                 | N/A                                                                                                                                                                                                                                                       |
| `scramble-table`                                        | N/A           | N/A    | N/A                                                                                                                            | [`cubing/scramble-table`](https://github.com/cubing/scramble-table)            | [`3338`](https://github.com/cubing/scramble-table/blob/4c33ac749fe79a3395c5bdaaaa869b3f25718224/script/dev.js#L6)         | N/A                                                                                                                                                                                                                                                       |

[^2]: Used by: <https://twizzle.net/stream>
[^3]: A record: `35.236.43.166`
[^4]: Shared
[^5]: [Verified](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages) for `github.com/cubing` ([config](https://github.com/organizations/cubing/settings/pages))

## Organizations

### GitHub

- URL: <https://github.com/cubing>
- Org settings URL: <https://github.com/organizations/cubing/settings/profile>
- 2FA enforcement for members:
  - Require two-factor authentication
    - Only allow secure two-factor methods
- Owners: `@lgarron`, `@jfly`

Certain repos have elevated privileges for maintainers. (TODO: document these.)

"Require two-factor authentication" and "Only allow secure two-factor methods" are enabled. This still leaves a lot of authentication options, and prevents a large class of potential risks. (Note that `@lgarron` worked on authentication at GitHub, and is very familiar with the security model, implementation, and tradeoffs.)

### `npm`

- URL: <https://www.npmjs.com/org/cubing>
- Org settings URL: <https://www.npmjs.com/settings/cubing/packages>
- 2FA enforcement for members: No (TODO)
- Owner: `@lgarron`
- Admin: `@jfly`

### `healthchecks.io`

- URL: (redacted)
- Owner: `@lgarron`
- Manager: `@jfly`

### Codeberg

- URL: <https://codeberg.org/cubing>
- Org settings URL: [text](https://codeberg.org/org/cubing/settings)
- Owner: `@lgarron`

Codeberg is an non-profit alternative to GitHub with a [principled mission](https://docs.codeberg.org/getting-started/what-is-codeberg/) that pushes back against what many see as hostile practices by GitHub. Projects may migrate there over time to avoid reliance on GitHub.

## Conventions

- We generally publish code under one of the following licenses:
  - Dedicate to the public domain using the [Unlicense](https://unlicense.org/).
  - MPL: for projects we want to encourage open collaboration for.
  - MIT: for projects with permissive usage.
  - GPL: Do not use for new projects. Use the MPL instead.
- Makefile conventions: <https://github.com/lgarron/Makefile-convention>, particularly: `make dev` and `make build`
- Files with a `.json` extension must contain valid JSON.
  - If using JSON5 or JSONC:
    - Prefer JSON5 ([which has a spec](https://spec.json5.org/)) over JSONC (an ad-hoc format that [Microsoft refuses to standardize](https://github.com/microsoft/vscode/issues/100688#issuecomment-2915925064) and which even Microsoft's tools parse and validate inconsistently).
    - Always use `.json5` or `.jsonc` file extensions. (Example: [`biome.jsonc`](https://github.com/lgarron/repo/blob/4dc160c59dae6cbb2740641dcecbfd99aa6296d9/biome.jsonc))
      - If a tool requires a use of a `.json` file extension (e.g. [TypeScript](https://github.com/microsoft/TypeScript/issues/43121)) and the file contents are not valid JSON, move the file to an adjacent `.jsonc` or `.json5` and symlink or reference the `.json` file path. (Example: [`tsconfig.json` → `tsconfig.jsonc`](https://github.com/cubing/cubing.js/blob/e5316667cba721cd275744270b030fddf0804eec/tsconfig.json))
- Add a `CI.yaml` GitHub Actions workflow with the following jobs when relevant. Do not use secrets for any workflows in this file.
  - `build`
  - `test`
- JS projects:
  - Language: TypeScript
  - Bundler: `esbuild`
  - Formatter: `biome`
- Rust:
  - When a nightly toolchain is needed (e.g. for the `portable_simd` feature), use `nightly-2025-10-01` for now. ([Examples](https://github.com/search?q=org%3Acubing+nightly-2025-10-01&type=code))

Many of these conventions are available in: <https://github.com/lgarron/ts-project-template>

# devcontainer-features

> One line in `devcontainer.json`. Your tools, ready to go.

[![Release](https://img.shields.io/github/v/release/devcontainer-env/devcontainer-features)](https://github.com/devcontainer-env/devcontainer-features/releases/latest)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Stop configuring developer devcontainer-features by hand in every container. Drop a feature reference into your `devcontainer.json` and get a consistent, reproducible environment — locally, in Codespaces, and in CI.

## Features

### `atlas`

Installs the [Atlas CLI](https://atlasgo.io) for managing database schemas as code.

```jsonc
{
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainer-env/features/atlas:1": {},
  },
}
```

#### Options

| Option    | Type   | Default  | Description                   |
| --------- | ------ | -------- | ----------------------------- |
| `version` | string | `latest` | Select the version to install |

---

### `psql`

Installs [psql](https://www.postgresql.org/docs/current/app-psql.html), the PostgreSQL interactive terminal.

```jsonc
{
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainer-env/features/psql:1": {},
  },
}
```

## Repository Structure

```
├── src
│   ├── atlas
│   │   ├── devcontainer-feature.json
│   │   └── install.sh
│   └── psql
│       ├── devcontainer-feature.json
│       └── install.sh
```

## License

MIT — use it, fork it, extend it.

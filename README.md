# Deploy to Gist

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/pentatonicfunk/action-gist-repo-sync.svg)](https://github.com/pentatonicfunk/action-gist-repo-sync/releases)

This is a Github Action to sync Github Repo to Github Gist.

## Quick start

```yml
- uses: actions/checkout@v3
- name: Gist Repo Sync
  uses: pentatonicfunk/action-gist-repo-sync@v1
  with:
    gist_token: ${{ secrets.GIST_TOKEN }}
    gist_id: from_gist_url
    source_path: my_path
```

## Setup

### Prep work

1. Create a gist (public or secret) if you don't have one.
1. Generate a new [Personal access token](https://github.com/settings/tokens/). Only the `gist` scope is needed.

### Project setup

1. Go to the repo **Settings > Secrets**. Add the generated token with name `TOKEN`.
1. Edit workflow file `.github/workflows/deploy.yml` as the example above.

### Options

#### `gist_token`

Personal access token for updating gist.

#### `gist_id`

Id portion from the gist url, e.g. `https://gist.github.com/pentatonicfunk/`**`867f66a0f25f9d4ca70adf1cf1944529`**.

#### `source_path` (optional)

Relative to the current repo's root directory, e.g. `dist-docs`. Default the repo directory it self `./`

## License

[MIT License](https://github.com/pentatonicfunk/action-gist-repo-sync/blob/main/LICENSE) ©
[pentatotnicfunk](https://github.com/pentatonicfunk)
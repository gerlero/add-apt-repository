# add-apt-repository

[![CI](https://github.com/gerlero/add-apt-repository/actions/workflows/ci.yml/badge.svg)](https://github.com/gerlero/add-apt-repository/actions/workflows/ci.yml)
[![Release](https://github.com/gerlero/add-apt-repository/actions/workflows/update-tags.yml/badge.svg)](https://github.com/gerlero/add-apt-repository/actions/workflows/update-tags.yml)

GitHub Action to add an APT repository (with its key) to the list of package sources.

## Usage

```yaml
- uses: gerlero/add-apt-repository@v1
  with:
    uri: http://example.com/repo
    key: url_or_path_to_key
- uses: gerlero/apt-install@v1
  with:
    packages: package
```

## Inputs

### `uri`

**Required**. The URI of the APT repository to add.

### `key`

The URL or path to the GPG public key file to use for authenticating the repository. Default: none.

### `suite`

The suite of the APT repository to add. Default: the codename of the distribution.

### `cache`

Whether to cache any installed prerequisite packages between runs. Default: `true`.

## Related actions

- [`gerlero/apt-install`](https://github.com/gerlero/apt-install): GitHub Action to install and cache APT packages.

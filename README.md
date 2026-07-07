# Inspire Planet Assets

This repository stores uploaded images and static assets for [inspireplanet.cc](https://github.com/sunling/inspireplanet.cc).

## Purpose

`inspireplanet-assets` is a dedicated asset repository for 启发星球, so user-uploaded images can be managed separately from the main application codebase.

## Structure

```text
user_uploads/
  └── image_<timestamp>_<random>.png
```

## Raw URL format

Uploaded images can be referenced with GitHub raw URLs:

```text
https://raw.githubusercontent.com/sunling/inspireplanet-assets/main/user_uploads/<filename>.png
```

## Migration source

Existing images are migrated from:

```text
sunling/inspireplanet.cc/user_uploads
```

A one-time GitHub Actions workflow is included at:

```text
.github/workflows/migrate-user-uploads.yml
```

It clones `sunling/inspireplanet.cc`, copies `user_uploads/` into this repository, and commits the migrated images if there are changes.

## App upload configuration

After migration, configure the app upload environment variables to point to this repository:

```text
GITHUB_REPO_OWNER=sunling
GITHUB_REPO_NAME=inspireplanet-assets
GITHUB_BRANCH=main
```

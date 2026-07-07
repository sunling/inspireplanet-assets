# Inspire Planet Assets

This repository stores uploaded images and static assets for [inspireplanet.cc](https://github.com/sunling/inspireplanet.cc).

## Purpose

`inspireplanet-assets` is intended to be a dedicated asset repository for 启发星球, so user-uploaded images can be managed separately from the main application codebase.

## Suggested structure

```text
user_uploads/
  └── <uploaded images>
```

## Migration source

Images are planned to be migrated from:

```text
sunling/inspireplanet.cc/user_uploads
```

After migration, the main app can update image references to point to this asset repository or its raw/CDN URLs.

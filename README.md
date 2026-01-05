# prymov-cli-tools
#!/bin/bash

## Description

Deletes files recursively in a given base directory based on a list of filename
patterns and a specific file extension.

This tool is designed as a lightweight CLI utility for maintenance and cleanup
tasks in E-Commerce environments.

---

## Typical E-Commerce Use Cases

- Removing outdated or incorrect product images
- Cleaning up asset directories after product deactivation
- Bulk deletion of media files by SKU, product ID, or variant code
- Maintenance of large image repositories in shop systems
- Cleanup after catalog imports or migrations

---

## Platform Compatibility

- **Linux only**
- Tested on **Debian**
- Requires GNU utilities

> This script is not compatible with Windows or macOS without GNU tools.

---

## Requirements

The following tools must be available on the system:

- `bash`
- `find` (GNU findutils)
- `rm` (GNU coreutils)

---

## Notes & Warnings

- This script permanently deletes files.
- Deleted files **cannot be recovered**.
- Always double-check:
    - Base directory
    - File extension
    - Filename patterns
- Consider testing with a small dataset first.

---

## Intended Audience

This tool is intended for:

- E-Commerce developers
- Shop administrators
- DevOps and system maintainers
- Anyone managing large media or asset directories in online shops

---

## Author

Arthur Prymov

---

## Lisense
MIT License

---
## Repository

https://github.com/oTreck/prymov-cli-tools


## How to use:

### Delete tools


#### delete-files-by-pattern.sh

Deletes files recursively in a given directory based on filename patterns
and file extension. Useful for bulk cleanup tasks.


Edit the configuration section inside the script to define:
- base directory
- file extension
- filename patterns

```
.delete/delete-files-by-pattern.sh /path/to/dir jpg id1 id2 id3
```


### Image tools

#### resize-images.sh

Recursively resizes image files to a fixed resolution.  
Designed for E-Commerce workflows where consistent product image dimensions
are required.

Typical Use Cases

- Standardizing product images before shop import
- Fixing inconsistent image sizes in existing catalogs
- Preparing media assets for marketplaces or PIM systems

```
.# resize-images.sh <BASE_DIR> <WIDTHxHEIGHT> <EXTENSION...>
./image/resize-images.sh ./product-images 443x665 jpg png

```
# prymov-cli-tools
A curated collection of reusable CLI tools and shell scripts for daily development, automation, and system maintenance.


## delete
### delete-files-by-pattern.sh

Deletes files recursively in a given directory based on filename patterns
and file extension. Useful for bulk cleanup tasks.


Edit the configuration section inside the script to define:
- base directory
- file extension
- filename patterns

```
.delete/delete-files-by-pattern.sh /path/to/dir jpg id1 id2 id3
```
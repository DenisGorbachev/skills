---
name: nushell
description: Use when reading or writing Nushell scripts. 
---

# Nushell

## Strings

- Must be quoted.

## Command invocations

- Must use long options for all commands except `cd`, `cp`, `mv`, `rm`, `mkdir`, `chmod`, `chown`.
- Should be direct (example: `^foo` instead of `^foo | complete`).
  - It raises an error on non-zero exit.
  - It trims the final newline.

## Scripts

- Must have a `nu` shebang.
- Must not rely on global state (e.g. `umask`)

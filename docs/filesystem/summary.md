# `File System: Summary`
This document outlines all the conventions and rules to be followed
regarding file systems.

## `Recognized File Systems`

Intercogni projects need to use either one or more of just the filesystem types
below:
- `exFAT/FAT64` (64-bit File Allocation Table)
- `NTFS` (New Technology File System)

> OS used must comply to being able to work with one or more of the choices above.

### `Configuring exFAT/FAT64 for Ubuntu`
Ubuntu images used to run Intercogni projects need to download `exfat-utils` through:

```bash
sudo apt install exfat-utils
```
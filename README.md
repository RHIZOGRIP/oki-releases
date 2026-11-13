# Oki releases

Downloads for Oki: https://keepoki.com/

Each release holds:

- `oki-<version>.exe`: the Windows installer. Download it and open it.
- `oki-<version>.zip`: the same release as a folder, for Linux or for a manual install.
- `SHA256SUMS` and `SHA256SUMS.minisig`: the checksums of both files, signed.

## Checking a download

In PowerShell, compare with the line in `SHA256SUMS`:

    Get-FileHash oki-<version>.exe -Algorithm SHA256

To check the signature of `SHA256SUMS` with [minisign](https://jedisct1.github.io/minisign/):

    minisign -Vm SHA256SUMS -P RWTqgYgvih8mgn6Xm9lx32sKVG6Fz5pFYcCHvOPFZy72Le/ftnTJsjoW

## Licence

Oki is licensed AGPL-3.0-only. The code it installs is on your computer, inside Oki, and you may read,
change and share it under that licence. The development repository is not public yet.

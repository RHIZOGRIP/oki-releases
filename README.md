# Oki releases

Downloads for Oki: https://keepoki.com/

Questions and discussion: https://discord.gg/gpumegdhR

Each release holds:

- `oki-<version>.exe`: the Windows installer. Download it and open it.
- `oki-<version>.zip`: the same release as a folder, for Linux or for a manual install.
- `SHA256SUMS` and `SHA256SUMS.minisig`: the checksums of both files, signed.

## Checking a download

In PowerShell, compare with the line in `SHA256SUMS`:

    Get-FileHash oki-<version>.exe -Algorithm SHA256

To check the signature of `SHA256SUMS` with [minisign](https://jedisct1.github.io/minisign/):

    minisign -Vm SHA256SUMS -P RWTqgYgvih8mgn6Xm9lx32sKVG6Fz5pFYcCHvOPFZy72Le/ftnTJsjoW

## Licences

Oki is put together from several works, each under its own licence:

- **Oki itself** (its management pages and service, its installer and launcher) and **the web
  connector**, `@rhizogrip/spore-plugin-web`: AGPL-3.0-only. If the AGPL does not suit
  your use, you can ask for a commercial licence at hi@keepoki.com.
- **spore**, the agent runtime Oki runs: Apache License 2.0.
- **mohdel**, which spore calls AI models through: MIT License.
- **Everything else**: Node.js, the Debian system Oki runs in, and several hundred npm and Debian
  packages, each under its own open-source licence.

Where to find them once Oki is installed, inside Oki:

- each npm package, with its licence file, is under `/opt/oki/node_modules`, and
  `/opt/oki/package-lock.json` lists them all with their versions;
- each Debian package has its licence at `/usr/share/doc/<package>/copyright`, and
  `/opt/oki/dpkg.txt` lists them all with their versions.

The development repositories of Oki and of the web connector are not public yet. Their code as
installed is on your computer, inside Oki, under the licence above.

# tasksai-programs

Builds of the programs [Tasks.ai](https://tasks.ai) provides to every task run, for programs that publish no
standalone build of their own. Today: poppler's PDF tools (`pdftotext`, `pdfinfo`, `pdftoppm`) with the libraries they
load, one folder per system (Linux x64 and ARM, macOS on Apple and Intel chips, macOS 11 or later).

Each release holds the bundles and the source of what they are built from. The bundles are assembled from
[conda-forge](https://conda-forge.org)'s packages by `scripts/poppler-bundle.mjs` in Tasks.ai's agents (reproducible:
the same bytes from the same pins), each listing its packages (`PACKAGES`) and their licences (`licenses/`).

Poppler is free software under the GNU GPL (version 2 or 3); its source for each release is attached to it, as
downloaded from [poppler.freedesktop.org](https://poppler.freedesktop.org). The libraries' sources are those of the
conda-forge packages named in `PACKAGES`.

Tasks.ai's computers do not download from here: each Tasks.ai site serves a copy, checked against the checksums in its
agents' lock.

# DataLab workspace capsule profile

This repository publishes the specification of the **DataLab workspace capsule** format at <https://datalab-platform.com/capsule/>.

A capsule (`.dlcapsule`) is a ZIP archive that holds a DataLab HDF5 workspace (`workspace.h5`) and an [RO-Crate](https://w3id.org/ro/crate/1.3) manifest (`ro-crate-metadata.json`). The manifest describes the processing provenance of the workspace data: which operations ran, with which parameters, on which input states, in which software environment, and which of them can be replayed and verified. Capsules can be exchanged between DataLab Desktop and DataLab-Web, and validated or inspected without either application.

## Published identifiers

| Resource | Identifier | Page |
| --- | --- | --- |
| Profile, version 0.1 (experimental) | `https://datalab-platform.com/capsule/0.1` | [0.1/index.html](0.1/index.html) |
| Terms (JSON-LD prefix `dlc`) | `https://datalab-platform.com/capsule/terms#` | [terms.html](terms.html) |

These identifiers are written into every capsule manifest. They are permanent: a published version keeps its meaning, a change of meaning gives a new profile version (`0.2`, …) next to the existing ones, and terms are only ever added.

The profile extends [RO-Crate 1.3](https://w3id.org/ro/crate/1.3) and [Process Run Crate 0.6](https://w3id.org/ro/wfrun/process/0.6).

## Reference implementation

[DataLab-Capsule](https://github.com/DataLab-Platform/DataLab-Capsule) is the Python library and command line that create, validate and inspect capsules (`workspace-capsule validate` and `workspace-capsule inspect`). It runs in CPython 3.9+ and in Pyodide, and needs neither DataLab, NumPy nor h5py to validate or inspect a capsule.

## Repository content

- `index.html`: landing page.
- `0.1/index.html`: profile 0.1 (archive layout, manifest requirements, manifest and state fingerprints).
- `terms.html`: definition of every `dlc:` term, one anchor per term.

The site is served by GitHub Pages under the `datalab-platform.com` domain of the DataLab Platform organisation.

## License

BSD 3-Clause, see [LICENSE](LICENSE).

# OpenAirClim Data

## Description
OpenAirClim is an open-source model for simplified evaluation of the approximate chemistry-climate impact of air traffic emissions.
The main model repository is available at https://github.com/dlr-pa/oac.
This repository contains the minimum pre-calculated response surface and background scenario data required to run OpenAirClim.

## Versioning
The data in this repository is versioned independently from the OpenAirClim model.
A new release is made here when there has been an update to the data.
Each release is automatically deposited at Zenodo: https://doi.org/10.5281/zenodo.22146822.
To ensure that new OpenAirClim model installations install this new data by default, please update `openairclim/repository.py` in the [main oac repository](https://github.com/dlr-pa/oac).

## Downloading the data
For detailed installation instructions, see https://openairclim.org/installation.html.
This installation method is required and possible for OpenAirClim v0.18 and higher.

Releases from this repository are synced with Zenodo.
The simplest way of downloading the data is to use the built-in method in OpenAirClim:

```bash
conda activate <env>  # or equivalent for venv/pyenv installations
oac-download-data
```

By default, this fetches the data version pinned by your installed ``openairclim`` release into a shared, per-user cache directory.
Some useful overrides:

```bash
# fetch a specific data version, or a specific Zenodo record/DOI
oac-download-data --version 1.2.0
oac-download-data --record 10.5281/zenodo.1234567

# download into a custom, one-off location (only affects this download)
oac-download-data --output-dir /path/to/data

# override the default cache location itself, so both downloads and
# config resolution consistently use it
export OPENAIRCLIM_DATA_DIR=/path/to/data
oac-download-data
```

Run ``oac-download-data --help`` for the full list of options.

Alternatively, this repository can be cloned using:

```bash
cd path/to/saving/location
git clone https://github.com/dlr-pa/oac-data.git
```

## Contributing
Contributions to the OpenAirClim model and data are very welcome.
Please read our [contribution guidelines](https://github.com/dlr-pa/oac?tab=contributing-ov-file) to get started.
Please open any issues related to the model and data in the [main oac repository](https://github.com/dlr-pa/oac), rather than here.
Pull requests are of course permitted in this repository.

## License
The OpenAirClim software is licensed under [Apache 2.0](https://github.com/dlr-pa/oac#Apache-2.0-1-ov-file).
The data in this repository is licensed under CC-BY-4.0, a copy of which can be found [here](LICENSE).

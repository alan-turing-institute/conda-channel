# conda-channel
Custom conda channel for building packages not currently available through conda

## Prerequisites
You will need a local `conda` installation. See [official instructions](https://conda.readthedocs.io/en/latest/) for details on how to set this up.

## Getting started
Make a new conda environment and activate it

```
conda create -y --verbose --name condachannel27 python=2.7
conda activate condachannel27
```

Install `conda build` which is needed for package creation and update your tools.

```
conda install -y conda-build
conda update conda
conda update conda-build
```

## Setting up build for a new package
To add a new build

```conda skeleton pypi --recursive <package name on pypi>```
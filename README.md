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
conda install conda-verify
```

## Setting up build for a new package
To add a new build

```conda skeleton pypi --recursive <package name on pypi>```

This will create the `<package name on pypi>` directory, containing `meta.yaml`. You may need to change this, the following resources can help you with this:

 - https://docs.conda.io/projects/conda-build/en/latest/concepts/recipe.html
 - https://python-packaging-tutorial.readthedocs.io/en/latest/conda.html
 - https://github.com/conda-forge/conda-forge.github.io/issues/345

## Running package builds
To run the build you can do the following:

```
conda build <package name on pypi>
conda build purge
```
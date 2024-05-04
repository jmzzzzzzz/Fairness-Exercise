# Fairness-Experiment-Tutorial
This is a tutorial for machine learning model fairness testing and mitigation.


## Experimental environment

We use Python 3.7 for our experiments. We use the IBM AI Fairness 360 (AIF360) toolkit to implement bias mitigation methods and compute fairness metrics. 

Installation instructions for Python 3.7 and AIF360 can be found at https://github.com/Trusted-AI/AIF360. That page provides several ways to install it. We recommend creating a virtual environment for it (as shown below), because AIF360 requires specific versions of many Python packages which may conflict with other projects on your system. If you would like to try other installation methods or encounter any errors during the installation process, please refer to the page (https://github.com/Trusted-AI/AIF360) for help.

#### Conda

Conda is recommended for all configurations. [Miniconda](https://conda.io/miniconda.html)
is sufficient (see [the difference between Anaconda and
Miniconda](https://conda.io/docs/user-guide/install/download.html#anaconda-or-miniconda)
if you are curious) if you do not already have conda installed.

Then, to create a new Python 3.7 environment, run:

```bash
conda create --name aif360 python=3.7
conda activate aif360
```

The shell should now look like `(aif360) $`. To deactivate the environment, run:

```bash
(aif360)$ conda deactivate
```

The prompt will return to `$ `.

Note: Older versions of conda may use `source activate aif360` and `source
deactivate` (`activate aif360` and `deactivate` on Windows).

### Install with `pip`

To install the latest stable version from PyPI, run:

```bash
pip install 'aif360'
```

[comment]: <> (This toolkit can be installed as follows:)

[comment]: <> (```)

[comment]: <> (pip install aif360)

[comment]: <> (```)

[comment]: <> (More information on installing AIF360 can be found on https://github.com/Trusted-AI/AIF360.)

In addition, we require the following Python packages. 
```
pip install sklearn
pip install numpy
pip install shapely
pip install matplotlib
pip install --upgrade protobuf==3.20.0
pip install fairlearn
```

## Dataset

We use the five default datasets supported by the AIF360 toolkit. **When running the scripts that invoke these datasets, you will be prompted how to download these datasets and in which folders they need to be placed.** You can also refer to https://github.com/Trusted-AI/AIF360/tree/master/aif360/data for the raw data files.




# Partial Gromov-Wasserstein with applications on Positive-Unlabeled Learning 

This code is an attempt to help reproduce results from the paper "Partial Gromov-Wasserstein with applications on Positive-Unlabeled Learning" https://arxiv.org/abs/2002.08276.

## Pre-requisites

This code is Python3 code and relies on the following libraries:

```
pot
math
numpy
pandas
matplotlib
sklearn
torch
torchvision
scipy
numba
geoopt
torch
mpl_toolkits
time
IPython
```

Dependencies can be installed via:

```bash
pip install -r requirements.txt
```

(maybe the `torch` dependency will raise an error and an alternative install method will be prompted).

## Available scripts

For figures 1 to 3, [notebook](Fig123.ipynb) that generate the figures is provided.

For tables 1 & 2, [notebook](tab12.ipynb) that generate the performances relative to the partial-W and partial-GW results is provided. The results regarding competitors have been obtained using the following github repository `https://github.com/MasaKat0/PUlearning` from the paper 

```
Masahiro Kato, Takeshi Teshima, Junya Honda 
Learning from Positive and Unlabeled Data with a Selection Bias. 
In ICLR, 2019.
```

To run notebook [tab12.ipynb](tab12.ipynb), first make the `data` folder with the following datasets:

- `mushrooms`, `shuttle.scale`, `shuttle.scale.t`, `usps`, `usps.t`, `connect-4`  from `https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/`
- `page-blocks.data`, `spambase.data` from `https://archive.ics.uci.edu/ml/index.php`
- `Caltech10_zscore_SURF_L10.mat`, `amazon_zscore_SURF_L10.mat`, `webcam_zscore_SURF_L10.mat` , `dslr_zscore_SURF_L10.mat`, `caltech_decaf.mat`, `amazon_decaf.mat`,`webcam_decaf.mat`, `dslr_decaf.mat` from ``https://github.com/jindongwang/transferlearning/blob/master/data/dataset.md#office+caltech`

(the MNIST dataset is automatically downloaded with `torchvision`).

### partial_gw.py

This is the script that contains the main function for computing partial-GW.  

Data come from the github repository 
`https://github.com/una-dinosauria/3d-pose-baseline` from the paper 

```
Julieta Martinez, Rayat Hossain, Javier Romero, James J. Little. 
A simple yet effective baseline for 3d human pose estimation. 
In ICCV, 2017.
```

### utils.py

This file contains functions to load the datasets, draw the different positive and unlabeled datasets and draw the figures.


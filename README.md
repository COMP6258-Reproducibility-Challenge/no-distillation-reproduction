# 6258-DPDL Reproducibility Challenge

The files in this repository are taken directly from: 
https://github.com/sunnytqin/no-distillation/tree/main

Most files include modifications used for running the extension experiments mentioned in the report.

## nodistill_GaussAndShuffle.py

This file is a modification of nodistill.py. It includes:
- the function add_noise, which lowers the probability of the true class using the argument --true_class_probability and adds random Gaussian noise to the remaining 99 labels. The function is found at line 332.
- a modified version of the function ablation_k, where rather than swapping the i-th top label with the last label, the top label is kept fixed and the remaining 99 labels are randomly shuffled. The function is found at line 288.

## no_distillation folder
This folder contains another modification of nodistill.py which add experiments for mixing noise into a percentage of images with the lowest soft label entropy.
- line 303: noise mixing code
- line 365: experimenting over various percentages of the data

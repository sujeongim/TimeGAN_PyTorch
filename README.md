# timegan-pytorch
This repository holds the code for the reimplementation of TimeGAN ([Yoon et al., NIPS2019](https://papers.nips.cc/paper/8789-time-series-generative-adversarial-networks)) using PyTorch. 

Lots of the code was derived from the pytorch implementation [here](https://github.com/d9n13lt4n/timegan-pytorch) and slightly modified to run with BG(Blood Glucose) level data.

> :warning: WARNING!!!
> - This implementation is written for other purposes, not for experiments in the original paper.
> - Lots of the code was derived from the pytorch implementation [here](https://github.com/d9n13lt4n/timegan-pytorch)


## Getting Started
### Installing Requirements
This implementation assumes Python3.8 and a Linux environment with a GPU is used.
```bash
cat requirements.txt | xargs -n 1 pip install --upgrade
```

### Directory Hierarchy
```bash
data/                         # the folder holding the datasets and preprocessing files
  ├ data_preprocessing.py     # the data preprocessing functions
  └ stock.csv                 # the example stock data derived from the original repo
metrics/                      # the folder holding the metric functions for evaluating the model
  ├ dataset.py                # the dataset class for feature predicting and one-step ahead predicting
  ├ general_rnn.py            # the model for fitting the dataset during TSTR evaluation
  ├ metric_utils.py           # the main function for evaluating TSTR
  └ visualization.py          # PCA and t-SNE implementation for time series taken from the original repo
models/                       # the code for the model
output/                       # the output of the model
main.py                       # the main code for training and evaluating TSTR of the model
requirements.txt              # requirements for running code
run.sh                        # the bash script for running model
visualization.ipynb           # jupyter notebook for running visualization of original and synthetic data
```

# NOIRE-Net - A convolutional neural network for automatic classification and scaling of high-latitude ionograms
This repository contains the code and data to reproduce the main results from the paper "NOIRE-Net - A convolutional neural network for automatic classification and scaling of high-latitude ionograms"
<img src="https://github.com/AndreasKvammen/NOIRE-Net/blob/main/logo.jpg?raw=true">

## Installation 
The scripts and functions in this repository can be used on you local machine by downloading a clone of this repository using: <br />
git clone https://github.com/AndreasKvammen/NOIRE-Net.git

This requires: 
 - GitHub (for cloning the repository)
 - Python, Jupyter and Tensorflow working together on your local machine. For this work, Python 3.10.9, JupyterLab Desktop 4.0.7 and Tensorflow 2.9.0 were used.

## Source
Contains the Jupyter Notebooks to train and test NOIRE-Net:
- E-classify-train: This Notebook trains the NOIRE-Net E-region classification networks
- E-classify-test: This Notebook tests the performance of the NOIRE-Net E-region classification networks
- F-classify-train: This Notebook trains the NOIRE-Net F-region classification networks
- F-classify-test: This Notebook tests the performance of the NOIRE-Net F-region classification networks
- E-scale-train: This Notebook trains the NOIRE-Net E-region scaling networks
- E-scale-test: This Notebook evaluates the NOIRE-Net E-region scaling performance
- F-scale-train: This Notebook trains the NOIRE-Net F-region scaling networks
- F-scale-test: This Notebook trains the NOIRE-Net F-region scaling networks
- NOIRE-Net-analyze: This notebook loads the trained NOIRE-Net models and automatically classifies and scales ionograms

## Data
Contains the replication data (input-output pairs) and auxiliary data used in the paper. The files use the epoch timestamp as their identifier. 
- train-test-val: This folder contains the 16776 input-output pairs used to develop NOIRE-Net
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information
- test-multi-human: This folder contains the 652 ionograms that were labeled and scaled by multiple human experts. The files use the epoch timestamp as their identifier along with the human initials (for the output .par files).
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information.
  3. NOIRE-Net-analyzed: contains classified and scaled ionograms in (.png) format, automatically processed by NOIRE-Net
  4. NOIRE-Net-analyzed-movie.mp4: is a movie of the .png images in the subfolder "NOIRE-Net-analyzed"
- test-24-hours: This folder contains the 1404 consecutive ionograms that were manually labeled and scaled. This folder also contains the auxiliary images from the all-sky camera in Kiruna, operated by the Swedish Institute of Space Physics.
  1. ionograms: contains the input ionograms in (.png) format with dimensions 310x310x1
  2. parameters: contains the output parameters in (.par) format with the manual labeling and scaling information
  3. NOIRE-Net-analyzed: contains classified and scaled ionograms in (.png) format, automatically processed by NOIRE-Net
  4. IRF-all-sky-images: contains the all-sky images acquired by the camera in Kiruna. See IRF-license.pdf for the license agreement before using this data.
  5. IRF-license.pdf: License agreement for data obtained from Kiruna Atmospheric and Geophysical Observatory at Swedish Institute of Space Physics
  6. NOIRE-Net-analyzed-movie.mp4: is a movie of the .png images in the subfolder "NOIRE-Net-analyzed"

## NOIRE-Net
Contains the trained convolutional neural networks (CNNs), jointly named NOIRE-Net. NOIRE-Net consists of CNNs specialized for 4 different tasks. 10 Networks were trained for each task. These networks are organized in subfolders named by their task:
- E-classify: contains the trained NOIRE-Net E-region classification networks
- F-classify: contains the trained NOIRE-Net F-region classification networks
- E-scale: contains the trained NOIRE-Net E-region scaling networks
- F-scale: contains the trained NOIRE-Net F-region scaling networks

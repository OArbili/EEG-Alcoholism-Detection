# Ensemble Learning for Alcoholism Classification Using EEG Signals

This repository provides a robust EEG classification algorithm for detecting Alcohol Use Disorder (AUD). By transforming the data into multiple representations—temporal features, frequency-domain signals, and image-based views—the approach trains diverse models (RNN, CNN, and fully connected layers) and merges them in a final ensemble. Subject-based cross-validation is used to avoid data leakage, ensuring reliable performance estimates. The resulting pipeline demonstrates high classification accuracy on a publicly available EEG dataset, surpassing baseline methods.

https://ieeexplore.ieee.org/document/10140181

## Key Features

- **Multimodal Data Processing**  
  - Converts 64-channel EEG signals into time-series features, frequency-domain representations, and 2D images  
  - Utilizes Fast Fourier Transform (FFT) and Independent Component Analysis (ICA) to enhance signal quality

- **Ensemble Learning Architecture**  
  - Recurrent Neural Networks (LSTM/Bi-LSTM) for sequence modeling  
  - EfficientNet-based Convolutional Neural Networks for image classification  
  - Fully Connected layers for tabular/feature-based input  
  - Final ensemble layer that combines model outputs to boost accuracy

- **Robust Evaluation**  
  - Employs subject-based (group) 5-fold cross-validation to prevent data leakage  
  - Achieves high classification accuracy when compared to other approaches on the same dataset

## Getting Started

1. **Install Dependencies**  
   - Clone this repository  
   - Install required Python packages from `requirements.txt`

2. **Download the Dataset**  
   - The EEG dataset is publicly available [here](https://archive.ics.uci.edu/ml/datasets/EEG+Database).  
   - Place the data files in the `/data` directory.

3. **Preprocessing & Training**  
   - Run the preprocessing scripts to transform raw EEG signals into time-series, frequency, and image forms.  
   - Use the training scripts to train all three models (RNN, CNN, FC).  
   - Finally, run the ensemble training script to combine their outputs.

4. **Evaluation**  
   - Evaluate performance via subject-based cross-validation  
   - Results and logs are automatically saved for analysis

## Citation

If you use this code or find our work helpful, please cite our paper:

> Cohen, S., Katz, O., Presil, D., Arbili, O., & Rokach, L. (2022).  
> **Ensemble Learning For Alcoholism Classification Using EEG Signals**. *IEEE Sensors Journal*.

## License

This project is licensed under the MIT License.


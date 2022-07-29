# Expert-level detection of pathologies from unannotated chest X-ray images via self-supervised learning

This repository contains code to train a self-supervised learning model on chest X-ray images that lack explicit annotations and evalute this model's performance on pathology-classification tasks.

## Data 
### Training Dataset
1. Navigate to [MIMIC-CXR Database](https://physionet.org/content/mimic-cxr/2.0.0/) to download the training dataset. 
2. Copy the dataset into the `data/` directory.
3. Navigate over to the `scripts/` directory.
3. Run `python preprocess_train_data.py`
4. This should preprocess the chest x-ray images into a hdf5 format used for training stored at `data/cxr.h5` and extract the impressions section as text from the corresponding chest x-ray radiology report stored at `data/mimic_impressions.csv` .

### Model Checkpoints
Model checkpoints of CheXzero pre-trained on MIMIC-CXR are publicly available at the following [link](https://drive.google.com/drive/folders/19YH2EALQTbkKXdJmKm3iaK8yPi9s1xc-?usp=sharing). Download files and save them in the `./models/` directory.

## Running Training
Run the following command to do CheXzero pretraining. 
```bash
python run_train.py
```
Use `-h` flag to see all arguments. 
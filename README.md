# SANSformers: Self-Supervised Forecasting in ELECTRONIC HEALTH RECORDS with Attention-Free Models

This repository is a reproduction of [SANSformers: Self-Supervised Forecasting in ELECTRONIC HEALTH RECORDS with Attention-Free Models](https://arxiv.org/pdf/2108.13672). 

## Requirements and Setup

 1. In order to access the MIMIC-IV v1.0 dataset, you need to be a credentialed user, complete the required training (CITI Data or Specimens Only Research), submit proof of completion of the required training, and sign the data use agreement for the project. Further instructions can be found at [MIMIC-IV v1.0 Dataset](https://physionet.org/content/mimiciv/1.0/)
 2. Once you have access, navigate to the Files section on the MIMIC-IV v1.0 dataset page and download the zip file.
 3. Unzip the file and upload the unzipped folder to your Google Drive; make sure the folder is located in MyDrive and is named `mimic-iv-1.0`
 4. Visit our [GitHub repository](https://github.com/catherinopew/CS598_DL4H) and download all files. It contains the necessary files to replicate our results.
 5. Visit this [Google Drive folder](https://drive.google.com/drive/folders/1P989oQuTRkMXTuptp0s59Z5VvtAZ1ohh?usp=sharing) and download all files. These are our model files that could not be uploaded to GitHub due to their large size.
 6. Navigate to your `mimic-iv-1.0` folder in MyDrive and add the following files to it:
    * config_additive_sansformer_ablation.yml
    * config_additive_sansformer_demo.yml
    * config_additive_sansformer.yml
    * config_axial_sansformer_ablation.yml
    * config_axial_sansformer_demo.yml
    * config_axial_sansformer.yml
    * mimic_test_rem2.feather
    * mimic_train_rem2.feather
    * pretrained_additive_model.pkl
    * pretrained_additive_model.pth
    * pretrained_axial_model.pkl
    * pretrained_axial_model.pth
    * results_log_ablations.csv
    * results_log.csv
    * sansformer_architecture.png
    * vectorizer.pickle
7. Visit our [Google Colab notebook](https://colab.research.google.com/drive/1899S4vPcBkohMXn5BAWzIAkrXN-mNssF?usp=sharing) and run each cell in order using the T4 GPU runtime type (if that's available; otherwise, use CPU).
    * The first cell will ask you to mount your Google Drive, so please log in with your Google account that has the `mimic-iv-1.0` folder.
8. (Optional) If you are interested in replicating the results of our ablation study, do steps 1-6 if you haven't already, visit this [Google Colab notebook](https://colab.research.google.com/drive/1bxDxmsi-hr2d-0LzeLIz1xpfpH4jg4n8?usp=sharing), and run each cell in order using the T4 GPU runtime type (if that's available; otherwise use CPU). 
    * Similar to step 7, the first cell will ask you to mount your Google Drive, so please log in with your Google account that has the `mimic-iv-1.0` folder.

## Pre-trained Models

As stated in the requires and setup, you can download the pretrained models here:
- [Pretrained Axial and Additive SANSformers models](https://drive.google.com/drive/folders/1P989oQuTRkMXTuptp0s59Z5VvtAZ1ohh?usp=sharing) 

## Results

Our model achieves the following performance on :

### [MIMIC-IV v1.0 Dataset](https://physionet.org/content/mimiciv/1.0/)

| Model name                       |      loss       |    bin_loss    |     auc_bin    |
| -------------------------------- |---------------- | -------------- | -------------- |
| Pretrained Additive SANSformer   |       66%       |       66%      |       66%      |
| Pretrained Axial SANSformer      |       67%       |       67%      |       67%      |

>📋  You can view more detailed results on our [main Google Colab notebook](https://colab.research.google.com/drive/1899S4vPcBkohMXn5BAWzIAkrXN-mNssF?usp=sharing).


## Contributing

>📋  Refer to LICENSE.txt on our GitHub repository for licensing information. We recommend cloning the provided Google Colab notebooks for your own use if you plan on making any contributions.

## References
Y. Kumar, A. Ilin, H. Salo, S. Kulathinal, M. K. Leinonen and P. Marttinen, "Self-Supervised Forecasting in 
Electronic Health Records with Attention-Free Models," in IEEE Transactions on Artificial Intelligence, doi: 10.1109/TAI.2024.3353164. keywords: {Medical services;Transformers;Data models;Predictive models;Computational modeling;Biological system modeling;Task analysis;Deep Learning;Electronic Health Records;Healthcare;Healthcare Utilization;Transfer Learning;Transformers},
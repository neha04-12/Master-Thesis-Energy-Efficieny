# Master-Thesis-Energy-Efficieny

This repository describes the detiled implementation of the master thesis project topic Enenrgy Efficiency in Buildings by detecting thermal anolamies using AI

This project was fullifiled under the partial requiremnt for the Master in Software engineering at Fachhochschule Techikum Wien, Austria and Masters in IT, Digitalization and Sustainability at Hochschule Luzern, Switzerland.

Abstract: This project aims at identifying heat anomalies in buildings from Aerial images using AI. The purpose of this project is to develop an ML model that identifies thermal leaks in buildings to tackle energy efficiency problems in buildings. This research utilizes the TBBR (Thermal Bridges on Building Rooftops) dataset which has high resolution images of aerial view of buildings and the corresponding annotations. This paper focuses on two main models, Faster RCNN and Masked RCNN. The selected models are trained on the TBBR dataset using pre-trained weights from pytorch libraries. The Faster RCNN model has two versions which each trained separately, showing different results. The first model detected some of the thermal anomalies accurately and wasn't able to capture some others. The second Version was able to predict the boxes more closely and accurately but still missed on capturing some of them. The MaskedRCNN model performed the best at capturing all the thermal anomalies. Some of the challenges that arose were due to the large size of the dataset and the huge dimensions of the images. This caused the input mismatch with the structure of the pretrained model architecture and the data loader format. This was tackled by scaling down the input dimension of the images and by creating custom dataset classes to feed to the pytorch data loader library. This helped streamline the training process. Another challenge was that the model would easily overfit or not converge even with the slightest difference in parameters like epochs and learning rate. To remedy this, multiple experiments to find the optimal number of epochs so as to prevent overfitting was identified and a learning rate scheduler was added to ensure the smooth convergence. There is still scope for improvement for future work with respect to model performance in terms of fine tuning parameters and model architecture. For example the anchor boxes can be redefined to target even smaller annotations which sometimes are left undetected in a few samples as compared to the larger instances.

The Implemented solution involves 4 main approaches with each of them being implemented in separate notebooks. 

The details of Data preprocesing and help to setup an download the dataset can be found in the first notebook
The Faster-RCNN with RESNET-50 backbone and FPN is impemnted in the second notebook
The Faster-RCNN with RESNET-50 backbone and FPN version 2 is implemnted in the third notebook
The Masked-RCNN with RESNET-50 backbone and FPN version 2 with Imagenet normalization is implemnted in the fourth notebook
The Masked-RCNN with RESNET-50 backbone and FPN version 2 is implemnted in the five notebook


The original dataset can be found here: https://zenodo.org/record/7022736
The description of the dataset can be found here: https://paperswithcode.com/dataset/tbbr

# Medical Landmark Detection - AI Research Intern Role Challenge

This repository contains an end-to-end deep learning regression pipeline designed to automatically detect and localise anatomical landmark coordinates from medical imagery. The architecture utilizes a deep residual network to predict eight continuous coordinates (4 x keypoints represented as x, y pairs).

The development, structuring, and reporting follow the formal guidelines requested by Origin Medical in **Screenshot 2026-06-04 085958.png** and **Screenshot 2026-06-04 090100.png**.

## Folder Structure

Origin_Project_Submission/
ÃÄÄ notebooks/
³   ÀÄÄ Landmark_Pipeline.ipynb  - Comprehensive Dataset, Dataloader, and Training script
ÃÄÄ outputs/
³   ÃÄÄ model.pth                - Serialized PyTorch weights of the trained ResNet18 model
³   ÀÄÄ loss_curve.png           - Exported training loss convergence plot
ÃÄÄ report/
³   ÀÄÄ Report.pdf               - Project report formatted strictly to Appendix-A guidelines
ÀÄÄ README.md                    - Project documentation and execution instructions

## Pipeline Mechanics
* **Data Pre-Processing & Normalization**: Absolute X-coordinates are scaled relative to the maximum width (x/800.0) and Y-coordinates are scaled relative to the maximum height (y/600.0). Input images are scaled and resized uniformly to (224, 224, 3).
* **Model Architecture**: Pre-trained **ResNet18** backbone where the default 1000-class classification block was swapped with a fully connected linear layer mapped to exactly **8 continuous output nodes**.
* **Hyperparameters**: Mean Squared Error (MSE Loss), Adam Optimizer (LR = 0.0001), Batch Size = 8, Epochs = 10.

## Candidate Information
* **Name**: Prajna S
* **USN**: 1by23et041
* **Department**: Electronics and Telecommunication Engineering (ETE)
* **Institution**: BMS Institute of Technology and Management (BMSIT)

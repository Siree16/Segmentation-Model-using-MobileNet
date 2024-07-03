# 🖥️ Segmentation Model Using MobileNet

Welcome to the Segmentation Model Using MobileNet repository for CSL7590. This assignment involves implementing transfer learning using MobileNet for image segmentation. The project is divided into three tasks. Follow the guidelines and instructions provided below to understand the solutions thoroughly.

## 📄 Table of Contents
- [General Instructions](#general-instructions)
- [Submission Guidelines](#submission-guidelines)
- [Objective](#objective)
- [Tasks](#tasks)
  - [Task 1: Pre-Processing](#task-1-pre-processing)
  - [Task 2: Feature Extraction](#task-2-feature-extraction)
  - [Task 3: Fine-Tuning](#task-3-fine-tuning)
- [Evaluation Metrics](#evaluation-metrics)
- [Solution Summary](#solution-summary)
- [Contact Information](#contact-information)

---

## General Instructions 📋
1. Clearly mention any assumptions you have made.
2. Report any resources you used while attempting the assignment.
3. Submissions in any other format or after the deadline will not be evaluated.
4. Add references to the resources used.
5. Plagiarism will result in zero marks.
6. Select the dataset correctly.

## Submission Guidelines 📑
1. Prepare a Python code file named `YourRollNo.py`. There should be only one .py file.
2. Submit a single report named `YourRollNo.pdf`, containing methods, results, and observations.
3. Provide your Colab file link in the report.
4. Upload both the code and report directly on Google Classroom.
5. Do not upload .ipynb files or screenshots in the report.

## Objective 🎯
Train a segmentation model using a MobileNet pre-trained on the ImageNet dataset as an encoder and design a decoder that predicts segmented masks. Evaluate the model's performance using various metrics.

## Tasks 🧪

### Task 1: Pre-Processing
- **Dataset**: Download the ISIC 2016 dataset.
  - Train: 900 training images.
  - Train masks: Segmented masks for training images.
  - Test: 379 test images.
  - Test masks: Segmented masks for test images.
- **Pre-Processing**: Resize images to 128x128 and apply necessary pre-processing steps like normalization and augmentation.
- **Custom Dataloader**: Design a custom dataloader for the dataset.

### Task 2: Feature Extraction
- **Network Architecture**: Use a pre-trained MobileNet encoder trained on ImageNetV1. Design a custom decoder for the segmentation task.
- **Training**: Train the decoder while keeping the encoder frozen. You may choose to take input for the decoder from the last layer of the encoder or from multiple layers.

### Task 3: Fine-Tuning
- **Network Architecture**: Keep the same architecture as in Task 2.
- **Training**: Train the segmentation model while fine-tuning the encoder weights.

## Evaluation Metrics 🧮
1. **Metrics**: Calculate and report the Intersection over Union (IoU) and Dice score.
2. **Plots**:
   - Training Loss
   - Validation/Testing Loss
3. **Analysis**:
   - Provide observations and analysis of the results.
   - Visualize several samples alongside their generated masks and ground truth.
   - Conduct a comparative analysis for both experiments.

## Solution Summary 📝

### Task 1: Pre-Processing
- **Dataset**: ISIC 2016 dataset with 900 training images and 379 test images.
- **Pre-Processing**: Images resized to 128x128 and normalized. Applied data augmentation techniques.

### Task 2: Feature Extraction
- **Network Architecture**: MobileNet encoder with a custom decoder.
- **Training**: Encoder weights frozen, only the decoder trained.

### Task 3: Fine-Tuning
- **Network Architecture**: Same as Task 2.
- **Training**: Both encoder and decoder weights trained.

### Results
- **Model 1 (Trainable Decoder)**:
  - Training Loss: 0.2896
  - Validation Loss: 0.2971
  - IoU: 0.6954
  - Dice Score: 0.7370
- **Model 2 (Frozen Decoder)**:
  - Training Loss: 0.3076
  - Validation Loss: 0.3347
  - IoU: 0.6823
  - Dice Score: 0.7176

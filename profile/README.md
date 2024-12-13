# Nutrisense: Smart Solution for Disease Detection and Food/Nutrition Recommendation
<p align="justify">According to the latest data from the World Health Organization (WHO) published in 2022, an estimated 390 million adults worldwide are underweight, and 149 million children under 5 suffer from stunting. Undernutrition remains a leading cause of death in young children, particularly in low- and middle-income countries. The consequences of undernutrition are far-reaching, affecting physical and cognitive development, as well as long-term health outcomes. One promising solution to address this growing global issue is the development of a nutrition-focused food recommendation application. This application could be designed to offer tailored meal plans that help individuals, especially those in vulnerable populations, meet their nutritional needs. By providing access to recipes that are nutrient-dense, affordable, and aligned with the dietary preferences of users, the app could empower people to make healthier food choices and improve their overall well-being. Such a platform would play a crucial role in combating undernutrition, reducing the prevalence of stunting, and improving health outcomes globally.</p>


## Themes 
<p align="justify">This project is focused on developing a personalized medical checkup application that provides tailored dietary recommendations based on users' individual health conditions. By collecting and analyzing key health metrics such as height, weight, blood pressure, and cholesterol levels, the app will offer customized food guidance that directly addresses the user’s unique health profile. The main goal of this application is to empower individuals to make informed, health-conscious food choices that align with their specific needs. Through predictive modeling, the app will be able to identify potential health risks and suggest appropriate foods that can mitigate those risks. In addition, the integration of computer vision technology will allow the app to analyze food images, offering users real-time, actionable dietary advice based on the foods they consume.</p>

<p align="justify">The second key component of this project is its focus on disease prevention and promoting overall wellness. By offering a personalized food safety analysis and nutrient-based recommendations, the app aims to proactively manage users' health and prevent chronic conditions such as diabetes, hypertension, and heart disease. With the ability to adapt to changing health metrics, the app will serve as a dynamic tool that evolves with the user’s health status, ensuring that dietary guidance remains relevant and effective over time. Ultimately, this solution will help users not only understand their current health condition but also make proactive, informed decisions about their diet that support long-term well-being.</p>

## Team Member 
### C242-PS384
| Bangkit ID | Name | Learning Path | University |LinkedIn |
| ---      | ---       | ---       | ---       | ---       |
| M312B4KY0972   | Dana Affan Rabbani | Machine Learning |  Universitas Sebelas Maret | <a href="https://www.linkedin.com/in/dana-arl/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| M312B4KY1701   | Handi Dwi Cahyo | Machine Learning | Universitas Sebelas Maret | <a href="https://www.linkedin.com/in/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| M312B4KY2310   | Luthfi Pratama Fauzie | Machine Learning | Universitas Sebelas Maret | <a href="https://www.linkedin.com/in/luthfi-pratama-fauzie-0492a224b/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| C283B4KY1436   | Fathur Rahman Nur Saputra | Cloud Computing | Universitas Negeri Semarang | <a href="https://www.linkedin.com/in/fathursaputra/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| C665B4KY3469   | Panca Ananda Putra | Cloud Computing | STMIK Kaputama |  <a href="https://www.linkedin.com/in/panca-ananda-putra-a581ab266/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| A200B4KY1340    | Fadlil Ferdiansyah  | Mobile Development | Universitas Diponegoro |  <a href="https://www.linkedin.com/in/fadlilfer/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |
| A811B4KY4082    | Satria Tarigan | Mobile Development | STMIK Time |  <a href="https://www.linkedin.com/in/satria-tarigan/"><img src="https://seeklogo.com/images/L/linkedin-logo-F84AF05CFC-seeklogo.com.png" style="width: 70px;"></a> |

## Preview App 
<br>
<img src="https://cdn.pixabay.com/animation/2023/07/19/01/41/01-41-18-281_512.gif" width="500">

## Resource 
### Machine Learning Resource

#### Disease Prediction Model
This module focuses on predictive modeling to analyze health metrics and symptoms for disease identification. It includes two models, which can be tested locally or deployed via Streamlit. Resource repository can be accessed from this link: [Disease Model Prediction](https://github.com/dana-ml27-bangkit2024/Capstone-C242-PS384_Project01)

#### Model 1: Health Data Prediction
- **Purpose**: Predict potential diseases based on health metrics such as height, weight, and blood pressure.
- **Features**:
  - Data preprocessing to combine and clean datasets.
  - Model training and evaluation, including metrics like accuracy.
  - Exporting trained models in HDF5 format.

##### Steps to Use:
1. **Environment Setup**:
   - Ensure Python 3.10.15 is installed in a Conda environment.
   - Install dependencies:
     ```bash
     pip install -r scripts/requirement-model1.txt
     ```

2. **Preprocessing Data**:
   - Combine datasets and save the processed file as `combined_dataset.csv`.

3. **Training the Model**:
   - Train the model using the preprocessed data.
   - Observe metrics during training, such as accuracy and loss.

4. **Saving the Model**:
   - The trained model is saved as an HDF5 file in the `models` directory.

5. **Testing the Model**:
   - Deploy and test locally or use TensorFlow.js conversion for web deployment.

#### Model 2: Symptom-Based Prediction
- **Purpose**: Predict diseases based on user-reported symptoms.
- **Features**:
  - Localized input support (e.g., Indonesian symptom mapping).
  - Real-time predictions based on user inputs.

##### Steps to Use:
1. **Environment Setup**:
   - Use the same environment as Model 1. No additional installations are needed.

2. **Input Symptoms**:
   - Provide symptoms in the supported language for accurate predictions.

3. **Prediction Output**:
   - View disease predictions based on symptoms.

#### Deployment
1. **TensorFlow.js Conversion**:
   - Convert HDF5 models to TensorFlow.js format using:
     ```bash
     !tensorflowjs_converter --input_format=keras models/disease-prediction-tf-model.h5 models/tfjs_disease_model
     !tensorflowjs_converter --input_format=keras models/symptoms_predict_model.h5 models/tfjs_symptoms_model
     ```
     Or:
     ```bash
     tensorflowjs_converter --input_format=keras models/disease-prediction-tf-model.h5 models/tfjs_disease_model
     tensorflowjs_converter --input_format=keras models/symptoms_predict_model.h5 models/tfjs_symptoms_model
     ```

2. **Streamlit Application**:
   - Run the application locally:
     ```bash
     streamlit run streamlit/app.py
     ```
   - Or access the deployed app: [Streamlit Deployment](https://capstone-c242-ps384-deploy-model.streamlit.app/).

#### Model 2: Food Detection by Image
  - Identifies food items and analyzes their nutritional value.
  - Helps provide dietary recommendations based on detected items.
  - Food and classification dataset:
      - [Nasi](https://universe.roboflow.com/ds/roXcbPZakq?key=IOK2pppuHi)
      - [Nasi Goreng](https://universe.roboflow.com/ds/lYlem1DICA?key=2HMTQg0rgF)
      - [Soto](https://universe.roboflow.com/ds/FQdVgKD4ne?key=tMg9wwKgp8)
      - [Paha Ayam Crispy](https://universe.roboflow.com/ds/FZfUvj19gl?key=ypVfBvWpXa)
      - [Dada Ayam Crispy](https://universe.roboflow.com/ds/9RrzjYG7zP?key=DGXSxu8utG)
      - [Ayam Panggang](https://universe.roboflow.com/ds/dT2udTcr7i?key=ETVBixn0SQ)
      - [Nugget](https://universe.roboflow.com/ds/UrSbFCrm4N?key=FNLSi6kwqh)
      - [Mie Goreng](https://universe.roboflow.com/ds/I8SK8dYvhn?key=vANvUfRlHa)
      - [Telur Mata Sapi](https://universe.roboflow.com/ds/qtDcjezMS7?key=MsTxOsLNqN)
      - [Telur Dadar](https://universe.roboflow.com/ds/cpGuB9lOVR?key=nrTvbBpPKd)
      - [Telur Rebus](https://universe.roboflow.com/ds/f1lrfXU9tb?key=atCgYFQ026)
      - [Kangkung](https://universe.roboflow.com/ds/JEpp5GrKG8?key=Q67vh9f99p)
      - [Tempe](https://universe.roboflow.com/ds/pthbuKQ9Ty?key=d9EsXhK7HX)
      - [Tahu](https://universe.roboflow.com/ds/mjRvU9VD2x?key=rwXLXDjT6K)
      - [Sosis](https://universe.roboflow.com/ds/eyPixVx3Zt?key=e8sEVbar9L)
      - [Burger](https://universe.roboflow.com/ds/RQ1i6ggeEI?key=DlCsNhQp9q)
      - [Rendang Sapi](https://universe.roboflow.com/ds/gStxqVxfkA?key=IVd936xzOi)
      - [Nutrition Fact](https://docs.google.com/spreadsheets/d/1snqE6leDkZlL61qQ4g-vUmiFjizJyN1OCVAhwWWKSm4/edit?gid=2024304766#gid=2024304766)
  # Food Object Detection and Classification

This repository contains implementations of two distinct approaches to tackle food object detection and classification as part of the **Bangkit 2024 Capstone Project.** The goal is to explore and develop efficient solutions for identifying and categorizing food items in images, using cutting-edge deep learning techniques.

---

### Project Structure

1. Normal CNN for Food Classification

    The normal_cnn directory contains the implementation of a standard Convolutional Neural Network (CNN) for image classification. This was an experimental approach aimed at understanding the fundamentals of food classification before diving into more complex detection models. It served as a preliminary step to:

   - Understand image classification using custom CNN architectures.
   - Experiment with dataset preprocessing, augmentation, and training strategies.

   - Build foundational knowledge for the subsequent Mask R-CNN implementation.

2. Mask R-CNN for Food Detection

    The mrcnn directory houses the implementation of Mask R-CNN, a state-of-the-art model for object detection and instance segmentation. This approach is the core of the project and focuses on detecting and segmenting multiple food items within an image.

    Mask R-CNN was chosen for its ability to localize and classify multiple objects, offering both bounding box detection and pixel-level segmentation. This makes it a powerful tool for applications such as food analysis and portion size estimation.

---
### Why Two Approaches?

 During the early phases of the project, the normal_cnn approach was implemented to experiment with classification techniques. The initial assumption was that Mask R-CNN could adapt and integrate a custom CNN architecture for classification tasks. However, upon deeper exploration, it became clear that Mask R-CNN operates differently, leveraging pre-trained backbones for feature extraction.

 This realization led to a pivot in focus towards implementing Mask R-CNN for detection and segmentation while retaining the normal_cnn implementation as a valuable learning experience. The knowledge gained from both approaches enriched the project, offering insights into:

 - Image classification fundamentals through CNNs.

 - Object detection and segmentation using advanced architectures like Mask R-CNN.

---

### Key Features

**Normal CNN**

- A straightforward convolutional architecture for classifying food images into predefined categories.
- Training pipeline includes data augmentation and validation.
- Insights gained through this implementation provided foundational knowledge for more advanced techniques.

**Mask R-CNN**

- Implementation leverages mrcnn for object detection and instance segmentation.

- Pre-trained backbones like ResNet101 are used for feature extraction.

- Custom configuration for training on food datasets, including:

    - Adjusted anchor scales for food object sizes.

    - Fine-tuning on specific layers for improved performance.

- Extensive use of data augmentation to improve robustness.

# Getting Started

### Conda Environment Setup

Before running any scripts, ensure you have set up the Conda environment using the provided `environment.yaml` file in the root directory. Run the following command to create the environment:

```bash
conda env create -f environment.yaml
```

Activate the environment using:
```bash
conda activate your_env_name
```

### Normal CNN

1. Navigate to the normal_cnn directory.

2. For training, run the Jupyter Notebook food_classification.ipynb.

3. For inference, execute the following script:
```bash
python food_inference.py
```

### Mask R-CNN

1. Navigate to the `mrcnn` directory.

2. Ensure you have installed the requirements from requirements.txt within the Conda environment.
```bash
pip install -r requirements.txt
```

3. The mrcnn directory mainly is organized into three key subdirectories:

   - training: Contains scripts for training the Mask R-CNN model. This includes:

       - A basic Mask R-CNN script for experimental purposes.

       - An advanced Mask R-CNN script for improved performance.

   - utils: Provides utility scripts for dataset preprocessing and randomization.

   - inference: Includes scripts for testing and generating predictions on new images.

For training or inference, simply run the respective Python scripts. Example:
```bash
python training/advanced_mrcnn.py

python inference/test_inference.py
```

# Deployment

The final Mask R-CNN model has been successfully deployed using Flask for scalability. Additionally, a local GUI has been developed for testing purposes. This GUI allows users to interact with the model, upload images, and visualize predictions in real-time. Both the Flask application and the GUI provide seamless access to the model’s detection and segmentation capabilities.

#### Key Files and Directories
- **`models/`**:
  - Contains trained models in HDF5 format and converted TensorFlow.js models.
- **`scripts/`**:
  - Scripts for data preprocessing, training, and testing models.
- **`app.py`**:
  - Streamlit application for user interaction and model deployment.


### Cloud Computing Resource

### Mobile Development Resource

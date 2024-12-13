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
     tensorflowjs_converter --input_format keras models/model1.h5 models/js_model/
     ```

2. **Streamlit Application**:
   - Run the application locally:
     ```bash
     streamlit run app.py
     ```
   - Or access the deployed app: [Streamlit Deployment](https://capstone-c242-ps384-deploy-model.streamlit.app/).

#### Food Image Analysis
- **Computer Vision**:
  - Identifies food items and analyzes their nutritional value.
  - Helps provide dietary recommendations based on detected items.
  - Further resource can be accessed from this link: [TFoodDetection](https://github.com/Wistchze/TFoodDetection)

#### Key Files and Directories
- **`models/`**:
  - Contains trained models in HDF5 format and converted TensorFlow.js models.
- **`scripts/`**:
  - Scripts for data preprocessing, training, and testing models.
- **`app.py`**:
  - Streamlit application for user interaction and model deployment.


### Cloud Computing Resource

### Mobile Development Resource

# 🌿 Fertilizer Recommendation System

A smart diagnostic tool to detect **nine nutrient deficiencies** across **three major crops** (rice, wheat, maize) in India. This tool uses **deep learning** to analyze leaf images and leverages additional farmer input to recommend the appropriate **fertilizer type and amount**, reducing costs and preventing overfertilization.

## 📚 Publication

This project is published in the *United International Journal for Research & Technology (UIJRT)*:

🔗 [Read the paper](https://uijrt.com/paper/nitrogen-deficiency-detection-paddy-urea-fertilizer-management)


## 🔍 Project Highlights
- 🌾 Targets major crops in India with high nutritional variability.
- 📈 Expanded dataset from 100 to 400+ images using augmentation techniques.
- 🧠 Developed CNN-based models trained on expert-labeled plant leaf images.
- 🧪 Integrates research-based rules from **Montana State University** and **USDA** for fertilizer recommendations.
- ✅ Achieved **88.24% final test accuracy** in identifying nutrient deficiency symptoms.

## 🧪 Crops & Nutrients Covered

### 🌱 Crops
- Rice
- Wheat
- Maize

### 💊 Nutrients
- Potassium
- Magnesium
- Zinc
- Iron
- Manganese
- Copper
- Boron
- Sulphur
- **Nitrogen** (only for rice)

## 🔁 Workflow

1. **User uploads a leaf image** showing early symptoms (e.g. chlorosis, necrosis).
2. The image is classified into 1 of 5 classes:  
   `['interveinal', 'margin', 'normal', 'spotty', 'tip']`.
3. **User provides**:
   - Leaf age (new / middle / old)
   - Presence of 4 additional symptoms (not visible in image)
4. A rule-based system maps symptoms to probable nutrient deficiencies.
5. Based on deficiency and crop type, the system **recommends appropriate fertilizers**.
6. Results are optimized to avoid overfertilization and reduce costs.

## 📁 Project Files

| File | Description |
|------|-------------|
| `fertilizer.xls` | Contains fertilizer information (2 sheets) used for recommendations. |
| `first_app.py` | Main Streamlit web application for users. |
| `200_epoch_97_87_soft.h5` | Trained CNN model to classify leaf images into 5 symptom classes. |
| `plain2model.tflite` | TFLite model for Nitrogen detection using rice leaf color classification. |
| `nn_model_basic.ipynb` | Jupyter notebook for CNN training. |
| `SessionState.py` | Utility for session management in Streamlit. |


## 📊 Results

- **Validation Accuracy**: 90%
- **Final Test Accuracy**: 88.24%

Detailed analysis and performance metrics are available in the `project_report` file.


## 📜 License

© All rights reserved.  
This project was completed as part of the Project-Based Learning (PBL) contest at **BMS Institute of Technology and Management**, Bengaluru, India.

**Team Members:**
1. Aishwarya M
2. Merlyn Mercylona Maki Reddy
3. Namrata Karki


## 💬 Acknowledgments

- Montana State University – Nutrient Deficiency Research
- USDA – Plant Nutrition Guidelines


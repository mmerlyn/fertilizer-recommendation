# 🌿 Fertilizer Recommendation System

A smart diagnostic tool designed to empower Indian farmers with accurate **nutrient deficiency detection** and **personalized fertilizer recommendations**, using deep learning and rule-based logic. By analyzing leaf images and combining them with contextual input, this system helps **reduce costs**, **improve yield**, and **prevent overfertilization** — especially for smallholder farmers without access to expert advice.

## Project Objective

To support data-driven fertilizer usage by identifying specific nutrient deficiencies in rice, wheat, and maize crops using:
- Leaf image classification via CNNs
- Additional user inputs (leaf age, visual symptoms)
- Rule-based mapping to nutrient deficiencies
- Fertilizer dosage recommendation based on land size and deficiency

## Impact

> More than 70% of Indian farmers are smallholders who rely on informal advice for fertilizer use. This often leads to **overapplication**, **yield loss**, and **environmental harm**.

This project addresses that by:
- Providing **instant, accurate diagnosis** via mobile or web
- **Reducing fertilizer waste** and costs by up to 40%
- Helping avoid **soil and water pollution** caused by excess runoff
- Encouraging **sustainable agriculture** through informed decisions

## Publication

The initial phase of this project was published in the *United International Journal for Research & Technology (UIJRT)*:

🔗 [Read the paper](https://uijrt.com/paper/nitrogen-deficiency-detection-paddy-urea-fertilizer-management)


## Highlights
- 🌾 Targets major crops in India: **rice, wheat, maize**
- 📈 Dataset expanded from 100 to 400+ images using augmentation
- 🧠 CNN model trained on real, labeled leaf image data
- ✅ Achieved **88.24% final test accuracy** in identifying nutrient deficiency symptoms
- 🧪 Research-based rules from Montana State University & USDA for fertilizer recommendation


## Crops & Nutrients Covered

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

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- Streamlit (for app UI)
- Pandas / NumPy / Matplotlib
- Excel (fertilizer database)

## ⚙️ Working

1. **User uploads a leaf image** showing symptoms (e.g. chlorosis, necrosis).
2. The image is classified into one of five categories:  
   `['interveinal', 'margin', 'normal', 'spotty', 'tip']`
3. User inputs:
   - Leaf age (new / middle / old)
   - Additional symptoms (stunted growth, red spots, twisted leaves, yellowing)
4. **Deficiency is predicted** based on model + rules
5. **Fertilizer type and quantity** are recommended using stored expert data
6. Land size input is used to calculate dosage precisely

## 📁 Project Files

| File | Description |
|------|-------------|
| `fertilizer.xls` | Fertilizer info for all crops and deficiencies |
| `first_app.py` | Streamlit web app UI |
| `200_epoch_97_87_soft.h5` | Trained CNN model (5 leaf classes) |
| `plain2model.tflite` | Nitrogen classifier (rice only, LCC based) |
| `nn_model_basic.ipynb` | CNN training notebook |
| `SessionState.py` | Streamlit session management helper |


## 📊 Results

- **Validation Accuracy**: 90%
- **Final Test Accuracy**: 88.24%

Model performance drops slightly on real webcam images vs. ideal training images, highlighting the importance of consistent preprocessing in deployment environments.

Detailed analysis and performance metrics are available in the `project_report` file.

## 📜 License

© All rights reserved.  
This project was undertaken in partial fulfillment of the requirements for the Bachelor of Engineering degree in Computer Science at BMS Institute of Technology and Management, Bengaluru, India.

**Team Members:**
1. Aishwarya M
2. Merlyn Mercylona Maki Reddy
3. Namrata Karki


## Acknowledgments

- Montana State University – Nutrient Deficiency Research
- US Department of Agriculture (USDA) – Fertilizer usage guidelines


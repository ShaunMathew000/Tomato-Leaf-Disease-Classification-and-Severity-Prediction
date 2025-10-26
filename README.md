# PDISA: Plant Disease Identification and Severity Assessment

## 🌿 **Project Overview**  
PDISA (Plant Disease Identification and Severity Assessment) is a deep learning-based solution for early detection and classification of plant diseases, with a focus on tomato leaf diseases. The model combines transfer learning, image segmentation, and predictive analytics to support agricultural sustainability and food security.

---

## ✨ Key Features

- **Disease Identification**: Utilizes a Convolutional Neural Network (CNN) architecture, primarily EfficientNet.
- **Severity Assessment**: Employs image segmentation techniques to quantify disease progression.

<img width="1272" height="839" alt="image" src="https://github.com/user-attachments/assets/2974007a-f336-4a54-b0ad-c3dc46d38703" />


## 💻 Technical Methodology

### Model Architecture

- **Primary Model**: EfficientNet (EfficientNetB3 for classification) was selected due to its superior accuracy and precision compared to alternatives like ResNet.
- **Transfer Learning**: Leverages ImageNet-pretrained models, with selective freezing of feature extraction layers and fine-tuning of the classification module.
- **Optimization**: Adam and RMSprop optimizers were tested; Adamax generally improved classification performance.

### Dataset and Scope

- **Dataset Source**: PlantVillage dataset.

- **Target Classes**:  

<img width="1054" height="564" alt="image" src="https://github.com/user-attachments/assets/c4c1219e-976e-4b1e-945b-f2394fb59b82" />

## 📊 Disease Severity Quantification

- **Method**: Image segmentation (color-based segmentation and thresholding) to isolate infected regions.
- **Severity Calculation**:  
  
  Severity % = (Infected pixels/Total leaf pixels) times 100
 
- **Severity Tiers**:  
  - Class 0: 0–5% (Healthy leaves)  
  - Class 1: 6–20%  
  - Class 2: 21–50%  
  - Class 3: 51–100% (Heavy infection)

---

## 📈 Performance and Results

<img width="1102" height="479" alt="image" src="https://github.com/user-attachments/assets/e7117d97-18ed-4053-b3aa-8389e20eebdc" />

<img width="1643" height="152" alt="image" src="https://github.com/user-attachments/assets/2f54012f-fd8e-44c7-854a-7e710bd90ffc" />


---

### Disease Severity Quantification
The **Severity Analysis Module** quantifies the progression of plant disease, a crucial step for delivering accurate treatment recommendations and effectively managing agricultural resources. The process utilizes specific libraries in OpenCV to implement severity prediction module.

#### Infected Region Isolation
The infected regions are isolated using **color-based segmentation** and **thresholding** methods. These steps convert the input image into a processed representation that highlights infected zones, enabling precise identification of diseased leaf areas.

#### Severity Calculation
The severity percentage is computed using the ratio of infected pixels to the total leaf pixels, multiplied by 100:


Severity % = (Infected Pixels/Total Leaf Pixels) times 100


<img width="870" height="492" alt="image" src="https://github.com/user-attachments/assets/d8c93936-357d-47a6-b694-6b557c75ef5c" />


#### Severity Tiers
Based on the computed severity percentage, leaves are categorized into four distinct severity classes:

| Class | Severity Range | Description                  |
|--------|----------------|------------------------------|
| 0      | 0–5%           | Healthy leaves               |
| 1      | 6–20%          | Mild infection               |
| 2      | 21–50%         | Moderate infection           |
| 3      | 51–100%        | Heavy infection              |

#### Validation
The severity estimation module confirmed its high reliability and robustness in quantifying disease progression.

<img width="1068" height="729" alt="image" src="https://github.com/user-attachments/assets/9054399b-5fb1-467d-8596-96f852d480ed" />



## 🚀 Getting Started

To run the PDISA model locally, download and run the tomatoClassification.ipynb and SeverityPrediction.ipynb files in the repository simultaneously.


## 📚 References

- PlantVillage Dataset  
- EfficientNet, ResNet, and ARIMA modeling documentation  
- Sustainable Development Goal 2: Zero Hunger


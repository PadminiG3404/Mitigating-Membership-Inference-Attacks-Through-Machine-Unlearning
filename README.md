# Mitigating Membership Inference Attacks Through Machine Unlearning 🔒

## Overview
This project explores **Machine Unlearning** techniques to mitigate **Membership Inference Attacks (MIA)** on deep learning models. We evaluate the impact of unlearning on privacy and model performance using **ResNet-18** trained on **CIFAR-10**. Our approach aims to remove sensitive data efficiently while preserving model accuracy and robustness.

## Methodology ⚙️
- Train a **ResNet-18** model on CIFAR-10.
- Evaluate **pre-trained model** performance on test and forget sets.
- Apply **machine unlearning** via fine-tuning and re-training.
- Measure **accuracy degradation** and **MIA resistance** post-unlearning.
- Compare **attack success rates** before and after unlearning.

## Getting Started 🚀
Run the project using Google Colab:  
[**Colab Notebook**](https://colab.research.google.com/drive/1wWMd_vaXp9ioNKQr_4pL2vxzVO3YdXhw?usp=sharing)  

Alternatively, download the `ipynb` file from this repository and run it in Jupyter Notebook.

## Dataset 📂
We use **CIFAR-10**, a dataset of **60,000 32x32 color images** across **10 classes**.

### Sample Images
Below are some images from the CIFAR-10 dataset:

![Sample CIFAR-10 Images](![image](https://github.com/user-attachments/assets/8594ab64-86ef-4f0c-86a9-591cdc9be05a)
)

## Results 📊

### Before Unlearning:
- **Train Set Accuracy**: **99.5%**
- **Test Set Accuracy**: **88.3%**

### After Unlearning:
- **Retain Set Accuracy**: **98.5%**
- **Test Set Accuracy**: **84.0%**

### Retrained Model:
- **Retain Set Accuracy**: **99.5%**
- **Forget Set Accuracy**: **88.2%**

### Attack Performance
The following histograms show the loss distributions before and after unlearning, along with the **attack accuracy of the Membership Inference Attack (MIA)**.

#### **Pre-trained vs. Fine-tuned Model**
![Pretrained vs Fine-tuned Model](![image](https://github.com/user-attachments/assets/d56643b1-873b-4b92-b8af-020af3f59dbf)
)

#### **Retrained vs. Fine-tuned Model**
![Retrained vs Fine-tuned Model](![image](https://github.com/user-attachments/assets/1f8dd895-7c60-4bce-a66c-ff046f447b17)
)

## Insights 🔎
- **Pre-trained models are highly vulnerable** to MIA, with an attack accuracy of **0.58**.
- **Unlearning reduces attack accuracy**, making it harder to infer whether a sample was in the training set.
- **Fine-tuning reduces attack accuracy to 0.51**, but it still retains some information from the forget set.
- **Retraining from scratch offers the best defense**, dropping attack accuracy to **0.50** while maintaining overall model performance.
- **Trade-off between privacy and accuracy**: Unlearning slightly reduces test accuracy but significantly enhances privacy.

## Applications 🔧
- **Privacy-Preserving AI**: Helps organizations comply with privacy regulations like **GDPR** and **CCPA** by allowing selective data removal.
- **Secure Federated Learning**: Ensures user data can be removed without retraining models from scratch.
- **Medical AI**: Protects sensitive patient data by enabling unlearning in healthcare models.
- **Financial Fraud Detection**: Helps maintain privacy in banking models while preventing membership inference attacks.

## Future Work 📌
- **Enhancing efficiency**: Developing faster unlearning methods to reduce computational costs.
- **Unlearning in Transfer Learning**: Investigating how unlearning affects **pre-trained large models**.
- **Adversarial Robustness**: Exploring the impact of unlearning on adversarial defenses.
- **Theoretical Foundations**: Strengthening the mathematical guarantees of unlearning in deep networks.
- **Dynamic Model Updates**: Integrating unlearning methods with models that undergo continuous training.

## Conclusion
- **Unlearning reduces MIA attack accuracy**, improving privacy protection.
- **Retraining is more effective than fine-tuning** in mitigating MIA.
- **Minimal accuracy degradation** is observed post-unlearning.

## Acknowledgement 🙏
We acknowledge the contributions of **researchers in privacy-preserving machine learning** and the open-source community for providing datasets and pre-trained models.


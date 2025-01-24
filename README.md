# Cats vs. Dogs Classification with MobileNetV2
This repository contains a machine learning project developed during the "BairesDev - Machine Learning Practitioner" bootcamp. 

The project focuses on classifying images of cats and dogs using the **MobileNetV2** architecture from TensorFlow with **transfer learning**. It demonstrates the application of pretrained models and data augmentation techniques on a standard dataset.

---

## Features

- Implements transfer learning using **MobileNetV2** pretrained on ImageNet.
- Processes the **"Cats and Dogs" dataset** from TensorFlow's ML resources.
- Utilizes data augmentation to improve model performance.

---

## Getting Started

To run this project on **Google Colab**:

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the notebook (`.ipynb` file) to your Google Drive or Colab environment.
3. Ensure that the Colab runtime is set to **Python 3** with **GPU** enabled:
   - Go to `Runtime` > `Change runtime type`.
   - Select `Python 3` as the runtime type and `GPU` as the hardware accelerator.
4. Run the notebook cell by cell:
   - The dataset will be automatically downloaded and extracted.
   - The training process will utilize the GPU for better performance.

---

## Results

### 1. Pretrained MobileNetV2 on ImageNet (without transfer learning)

The model was tested using an image of a Sphynx cat. Below are the **top 5 predicted classes** and their probabilities:

| Rank | Class          | Probability |
|------|----------------|-------------|
| 1    | wool           | 5.73%       |
| 2    | French_bulldog | 4.90%       |
| 3    | hog            | 4.72%       |
| 4    | hammer         | 3.86%       |
| 5    | lab_coat       | 3.11%       |

The pretrained MobileNetV2 struggled to accurately classify the image, likely due to its training on a broad set of ImageNet classes, not specifically tailored for cats and dogs.

---

### 2. MobileNetV2 after Transfer Learning

After fine-tuning the MobileNetV2 model with transfer learning, the same image of a Sphynx cat was tested again. The results were as follows:

- **Predicted Class**: cat  
- **Probability**: 99.56%

The fine-tuned model performed significantly better, correctly classifying the image as a cat with high confidence.

---

## References

- Dataset: [Cats and Dogs Filtered](https://storage.googleapis.com/mledu-datasets/cats_and_dogs_filtered.zip)
- Framework: TensorFlow 2.x

---

## Acknowledgments

This project was developed as part of the **"BairesDev - Machine Learning Practitioner"** bootcamp.

# Part 2: Computer Vision – CNN Prototype

## Task 1: Problem Identification

The given dataset represents an image classification problem.

The objective is to classify product surface images into one of four categories: normal, scratch, dent, and stain. Each image is associated with a single label indicating the type of surface condition.

Image classification is appropriate for this dataset because each image belongs to one class, and there is no requirement to localize defects or perform pixel-level segmentation.

Therefore, a multi-class classification approach using a Convolutional Neural Network (CNN) is suitable for solving this problem.

---

## Task 2: Dataset Exploration
The dataset consists of four classes: **dent, normal, scratch, and stain.** Each class contains **120 images,** resulting in a total of **480 images.**

The dataset is **perfectly balanced,** as all classes have an equal number of images. This ensures that the model will not be biased toward any particular class during training and can learn each category effectively.

To better understand the data, sample images from each class were visualized. These images clearly show distinct surface conditions:

- Dent images contain visible deformations
- Scratch images show linear surface damage
- Stain images contain irregular colored patches
- Normal images represent clean, undamaged surfaces

All images in the dataset have a fixed dimension of **96 × 96 pixels,** which simplifies preprocessing and allows consistent input to the CNN model.

Overall, the dataset is clean, well-structured, and balanced, making it highly suitable for a **multi-class image classification task.**

---

## Task 3: Image Preprocessing
(To be added)

---

## Task 4: CNN Model Creation
(To be added)

---

## Task 5: Model Training and Evaluation
(To be added)

---

## Task 6: CNN Concept Explanation
(To be added)

---

## Task 7: Business Use Case Mapping
(To be added)

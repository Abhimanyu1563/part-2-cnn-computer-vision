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
The image data was preprocessed to make it suitable for training a CNN model.

All images were resized to a fixed dimension of **96 × 96 pixels** to ensure consistency in input shape. Pixel values were normalized by scaling them to the range **[0, 1],** which helps improve model convergence during training.

The dataset was split into training and validation sets using an **80:20 ratio.** This allows the model to be evaluated on unseen data during training.

Additionally, data augmentation techniques such as slight rotation, zooming, and horizontal flipping were applied to the training data. This helps improve generalization and reduces the risk of overfitting, especially given the relatively small dataset size.

---

## Task 4: CNN Model Creation
A Convolutional Neural Network (CNN) was developed using TensorFlow/Keras to perform multi-class classification on the image dataset.

The architecture consists of three convolutional blocks. Each block includes a Conv2D layer with ReLU activation followed by a MaxPooling layer. These layers progressively extract spatial features such as edges, textures, and structural patterns while reducing the spatial dimensions of the input.

After feature extraction, a Flatten layer converts the 2D feature maps into a 1D vector. This is followed by a fully connected Dense layer with 128 neurons, which helps the model learn higher-level representations.

The final output layer consists of 4 neurons with Softmax activation, corresponding to the four classes: dent, normal, scratch, and stain. This allows the model to output class probabilities for multi-class classification.

The model was compiled using the Adam optimizer and categorical crossentropy loss function, which is well-suited for multi-class classification tasks.

The total number of trainable parameters in the model is approximately 1.7 million, providing sufficient capacity to learn meaningful visual patterns from the dataset.

---

## Task 5: Model Training and Evaluation
_Overview_

In this task, the Convolutional Neural Network (CNN) model was trained and evaluated on the image dataset containing four classes: dent, normal, scratch, and stain.

_Training Performance_

The model was trained over multiple epochs, and both training and validation metrics were tracked.

**Accuracy & Loss Curves**
- Training accuracy steadily increased and reached near-perfect levels (~99–100%).
- Validation accuracy closely followed the training curve, indicating good generalization.
- Loss decreased consistently for both training and validation sets.
- No major divergence between curves → no strong overfitting observed.

**Confusion Matrix**
- The confusion matrix shows predictions across all four classes.
- The model is able to classify all categories but with some misclassifications between similar classes.
- Classes like dent and scratch appear slightly confused in certain cases.
- Overall, the distribution suggests the model has learned meaningful patterns but is not perfect.

**Sample Predictions**
- The model correctly identifies normal, dent, and stain in most cases.
- Predictions align well with visible features in the images.
- This demonstrates that the CNN is learning visual patterns effectively.

_Key Observations_
- High accuracy (~98–99%) indicates strong model performance.
- Balanced dataset (equal samples per class) helped stable learning.
- Minor confusion between visually similar defects still exists.
- Model generalizes well without significant overfitting.

_Conclusion_
The CNN model performs effectively on the classification task, achieving high accuracy and stable training behavior. While performance is strong, further improvements could be made by:
- Increasing model depth or tuning hyperparameters
- Applying data augmentation
- Using more complex architectures (e.g., transfer learning)

---

## Task 6: CNN Concept Explanation
(To be added)

---

## Task 7: Business Use Case Mapping
(To be added)

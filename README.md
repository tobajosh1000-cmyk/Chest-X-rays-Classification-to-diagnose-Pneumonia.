# Chest-X-rays-Classification-to-diagnose-Pneumonia.
This project focuses on building a Convolutional Neural Network (CNN) for the
binary classification of chest X-rays to diagnose Pneumonia. The work was carried out in
structured stages, utilizing a curated dataset of medical images to train a custom-built AI model.

## Data Preparation
 Curated a balanced dataset of chest X-rays divided into distinct classes: Normal and
Pneumonia.
 Structured the data into specific splits to ensure controlled training and evaluation:
o Training Set: 32 images (16 Normal, 16 Pneumonia) to teach the model features.
o Validation Set: 10 images (5 Normal, 5 Pneumonia) to tune performance during
training.
o Testing Set: 16 images (8 Normal, 8 Pneumonia) for final unbiased evaluation.

## Data Preprocessing
 Implemented ImageDataGenerator to handle image loading and preprocessing
automatically.
 Resizing: Configured the data flow to resize all input X-rays to a uniform dimension of
150x150 pixels
 Normalization: Applied pixel scaling by a factor of 1/255 to normalize intensity values
between 0 and 1, facilitating stable model convergence.
 Batching: Set a batch size of 10, allowing the model to update weights after processing
small groups of images.

## Model Development
 Architecture: Designed and built a custom Convolutional Neural Network (CNN) from
scratch rather than using pre-trained models.

 Layer Design: Constructed specific convolutional layers to extract spatial features from
the X-rays, allowing the model to learn patterns such as lung opacity and structural
definitions unique to pneumonia.
 Output: Configured the final dense layer to output a single probability score suitable for
binary classification.

## Training
 Trained the model for 10 epochs, monitoring the learning process as the model iterated
through the training data.
 Used the validation set (5 Normal, 5 Pneumonia) to check the model&#39;s performance at the
end of each epoch, ensuring the model was not just memorizing the training data.

## Model Evaluation
 Testing: Deployed the trained model on an unseen testing set of 16 images (8 Normal, 8
Pneumonia).
 Inference: Generated individual predictions for each test image, resulting in probability
scores (e.g., 0.448, 0.472) and a final classification label (e.g., &quot;is pneumonia&quot;).
 Analysis: Analyzed the raw probability outputs to understand the model&#39;s confidence
levels and diagnosis consistency across different patient scans.

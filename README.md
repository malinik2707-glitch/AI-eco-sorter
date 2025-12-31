# AI-eco-sorter
7 days mini project using python ,aiml

# ✍DAY-1 DATASET COLLECTION & PREPARATION :)

__PROJECT OVERVIEW__

Eco sorter is AI system that classifies waaste into different categories automatically.On Day-1, we focused on collecting and organizing dataset,which is the foundation for training the AI model.

🔔OBJECTIVE 
* Finalize waste categories
* collect images for each class from online sources and manual curation
* organize dataset for AI training


📂GOOGLE DRIVE DATASET LINK:

The dataset is uploaded to google drive due to size limitations on github.
here we go 👉 <https://drive.google.com/file/d/1dVgasfuLaY5RVPZus7lVIBnjRKdxMHI_/view?usp=sharing>

# 📁DATASET CONTAINS
- Recyclable
- non-Recyclable
- Organic
- Hazardous
- Medical waste

** WASTE CATEGORIES**
1.Recyclable - plastic bottles,paper,metal cans,glass etc..
2.Non-Recyclable - Wrappers,dirty plastics,mixted waste etc..
3.Organic/Biodegradable - Food waste,leaves,vegetables peels etc..
4.Hazardous - batteries,pesticides,paints,e-waste...

DATASET COLLECTION
> Image collected from google images and existing datasets
> Added medical waste images manually
> Removed duplicate and unclear images
> Organized dataset into foldes per class

ISSUES/CHALLENGES

< some images were distrubing; only safe items were retained
< slight imbalance in image numbers between classes

## DAY 2- PREPROCESSING

It includes resizing images,converting to rgb/grayscale and displaying histograms.The preprocessing ensures the dataset is ready for cnn training.

FEATURES:
> load images from dataset folders train/test/validation.
> Resize images to a standard size 224x224
> convert images to RGB TO CNN input
> convert images to grayscale from histogram visualization
> display grayscale histogram for understanding pixel intensity


## DAY 3 - Normalization & CNN MODEL DESIGN

 Day 3 fouses on preprocessing and cnn model design for echo sorter.The steps include image normalization, grayscale convertion and cnn architecture design for feature extraction.

 FEATURES:

 > normalize pixel values 0-1 range for faster convergence
>  histogram visualization to analyze pixel intensity distribution
> cnn model design
> INPUT-CONV2D-MAXPOOLING-CONV2D-MAXPOOLING-DENSE-DROUPOUT-OUTPUT LAYER

OUTPUT:

    ┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┓
┃ Layer (type)                    ┃ Output Shape           ┃       Param # ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━┩
│ conv2d_6 (Conv2D)               │ (None, 222, 222, 32)   │           896 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ max_pooling2d_6 (MaxPooling2D)  │ (None, 111, 111, 32)   │             0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ conv2d_7 (Conv2D)               │ (None, 109, 109, 64)   │        18,496 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ max_pooling2d_7 (MaxPooling2D)  │ (None, 54, 54, 64)     │             0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ conv2d_8 (Conv2D)               │ (None, 52, 52, 128)    │        73,856 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ max_pooling2d_8 (MaxPooling2D)  │ (None, 26, 26, 128)    │             0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ flatten_2 (Flatten)             │ (None, 86528)          │             0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_4 (Dense)                 │ (None, 128)            │    11,075,712 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dropout_2 (Dropout)             │ (None, 128)            │             0 │
├─────────────────────────────────┼────────────────────────┼───────────────┤
│ dense_5 (Dense)                 │ (None, 5)              │           645 │
└─────────────────────────────────┴────────────────────────┴───────────────┘
 Total params: 11,169,605 (42.61 MB)
 Trainable params: 11,169,605 (42.61 MB)
 Non-trainable params: 0 (0.00 B)

 ## DAY 4 - MODEL TRAINING


📌 Task of the Day

Today we focused completely on training the CNN model for our Eco-Sorter waste classification project.

🎯 Objectives

✔️ Load the prepared dataset
✔️ Build the CNN model
✔️ Train the model
✔️ Monitor accuracy & loss
✔️ Save trained model

Dataset contains image categories such as:

🧃 Plastic

📰 Paper

🥫 Metal

🍌 Organic

🧱 medical waste


👉 Images were resized to 224 × 224
👉 Pixel values were normalized between 0 and 1

🧩 Model Architecture

We used a Convolutional Neural Network (CNN) containing:

🔹 Convolution layers
🔹 Max-Pooling layers
🔹 Dropout layer (to reduce overfitting)
🔹 Dense fully-connected layer
🔹 Softmax output layer

Optimizer → Adam
Loss → Categorical Crossentropy
Metric → Accuracy

🏋️‍♂️ Training Details

📌 Model trained using:

Epochs: 10–20

Batch size: 32

Data augmentation applied:

rotation

zoom

flip


📊 Result Visualizations

📈 Accuracy Graph

Displays:

🔵 Training Accuracy
🟠 Validation Accuracy

Used to observe learning progress.

📉 Loss Graph

Displays:

🔵 Training Loss
🟠 Validation Loss

Used to detect overfitting/underfitting.

🔥 Additional Evaluation

We also generated:

✅ Confusion Matrix
✅ Heatmap Visualization

Helps analyze true vs predicted classes.

🏆 Outcome

✔️ CNN model successfully trained
✔️ Performance metrics plotted
✔️ Model saved for testing

## DAY 5- MODEL EVALUATION

Objective

Evaluate the trained CNN model on test images to measure its performance in classifying different waste types such as plastic, paper, metal, glass, and organic.

Steps Performed

1. Load the Trained Model
      The CNN model trained on preprocessed images was loaded for evaluation.

2. Prepare Test Data

Test images were loaded and rescaled to match the model input size.
Data was structured into folders according to classes: plastic, paper, metal, glass, organic.

3. Model Evaluation

The model was evaluated using metrics:

Test Loss – measures the difference between predicted and actual labels.
Test Accuracy – percentage of correctly classified images.


4. Confusion Matrix Analysis

A confusion matrix was generated to analyze per-class performance.
This shows which classes the model predicts well and where it might make errors.


5. Visualization

Heatmaps were plotted to visually represent the confusion matrix.
This makes it easier to interpret the model’s predictions across classes.

## DAY 6- PREDICTION
Observations

The model shows high accuracy for classes with more training images.
Some misclassifications may occur for visually similar waste types.
Confusion matrix provides a clear view of strengths and weaknesses in classification.

Objective

Use the trained CNN model to predict the class of unseen medical waste images and demonstrate how the ECO sorter can classify items such as bandages, plastic, glass, metal, and paper.

Steps Performed
1. Load Trained Model
The CNN model trained on medical waste images was used for prediction.

2. Prepare Input Images
Single or multiple test images were preprocessed:
Resized to the model input size (224×224 pixels)
Pixel values scaled between 0 and 1

3. Prediction Process
Each input image was fed into the model.
The model outputs predicted class probabilities.
The class with the highest probability was selected as the predicted class.

4. Results Analysis
Predicted labels show the type of medical waste for each image: Bandage, Plastic, Glass, Metal, Paper.
Confidence scores indicate how certain the model is about its prediction.

5. Visualization
Images were displayed alongside their predicted class and confidence to clearly show model predictions.

Observations / Expected Outcomes
The model predicts correctly for most clearly distinguishable waste types.
Some misclassifications may occur for visually similar items.





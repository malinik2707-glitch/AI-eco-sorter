# AI-eco-sorter
7 days mini project using python ,aiml

# DAY-1 DATASET COLLECTION & PREPARATION :)

__PROJECT OVERVIEW__

Eco sorter is AI system that classifies waaste into different categories automatically.On Day-1, we focused on collecting and organizing dataset,which is the foundation for training the AI model.

__OBJECTIVE OF DAY-1__
* Finalize waste categories
* collect images for each class from online sources and manual curation
* organize dataset for AI training


📂GOOGLE DRIVE DATASET LINK:

The dataset is uploaded to google drive due to size limitations on github.
here we go 👉 <https://drive.google.com/file/d/1dVgasfuLaY5RVPZus7lVIBnjRKdxMHI_/view?usp=sharing>

# DATASET CONTAINS
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


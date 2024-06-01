# Documentation

Welcome to the official documentation for GoodModelBadModel. This service allows users to compare outputs from different machine learning models, focusing on semantic segmentation. Here you'll find detailed instructions and guidelines on how to effectively use our service.

### **Table of Contents**

1. Overview
2. Key Concepts
3. Uploading Data

### **1. Overview**

GoodModelBadModel is a unique service dedicated to comparing machine learning models' outputs. Currently, our focus is on semantic segmentation models. This documentation aims to guide you through the various functionalities our service offers and to help you understand how you can use it to enhance your model evaluation strategies.

### **2. Key Concepts**

Before diving into the details, it's important to understand a few key concepts related to our service. These concepts are critical for understanding how our system organizes data and results.

- **Dataset**: A collection of images along with their segmentation classes. Each dataset contains information such as class-to-color mappings and class names.
  
- **Image**: Represents an individual image file within a dataset. Images are linked to specific datasets.
  
- **Model**: In the context of our service, a model represents a specific machine learning model whose outputs (segmentations) you wish to compare. Each model is associated with a dataset.

- **Label**: A label represents the output of a model for a particular image, showing the segmented classes.

- **Model Difference and Improvement**: These are measurements and visualizations that compare the outputs of different models to each other and to a ground truth, if available.


### **3. Uploading Data**

The ability to [upload](https://goodmodelbadmodel.com/ingestion/upload-dataset/) data correctly is crucial for using GoodModelBadModel. Here's a detailed guide on how to prepare and upload your data:

- **Dataset Zip File Structure**: Your zip file should include a main folder named after your dataset. This folder should contain:
  - `classes.json`: A JSON file defining the mappings from class indices to colors and names for visualization and analysis.
  - `images/`: A directory containing all the image files you wish to analyze.
  - `models/`: A directory with subdirectories for each model output you want to compare.

**Example Zip Structure:**
```
cityscapes_10/
   - classes.json
   - images/
     - 1.png
     - 2.png
   - models/
     - Model1/
       - 1.png
       - 2.png
     - Model2/
       - 1.png
       - 2.png
     - Model3/
       - 1.png
       - 2.png
```

**Example class.json content**

```json
[
  {
    "class_id": 0,
    "class_name": "unlabeled",
    "color": [0, 0, 0],
  },
  {
    "class_id": 1,
    "class_name": "oranges",
    "color": [255, 165, 0],
      
  }
]
```


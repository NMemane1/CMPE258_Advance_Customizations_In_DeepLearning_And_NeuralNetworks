# CMPE 258 Assignment 4 – Regularization, Augmentation, Custom Deep Learning Constructs, and Experiment Tracking

This repository contains my work for **CMPE 258 Assignment 4**.  
I organized the assignment into **11 Colabs**.

- **Colabs 1 through 6 cover Part 1**
- **Colabs 7 through 11 cover Part 2**

To keep the assignment consistent across notebooks, I used one synthetic multimodal dataset family called the **Student Wellness dataset**. This dataset includes multiple modality-specific subsets such as:
- image data
- text data
- tabular data
- time series data

Using one common dataset family helped me compare different deep learning techniques more consistently instead of switching to unrelated datasets in every notebook.

---

# Repository Structure

## Part 1 – Augmentation, Regularization, and Generalization
**Covered in Colabs 1–6**

### Colab 1 – Regularization Techniques in TensorFlow and PyTorch
This notebook focuses on regularization and generalization techniques for image classification in both TensorFlow and PyTorch.

Main ideas covered:
- baseline image classifier
- L2 regularization / weight decay
- dropout
- batch normalization
- early stopping
- initialization comparison
- Monte Carlo dropout
- A/B-style comparison of validation and test performance

This notebook is mainly about understanding how model generalization changes when different regularization strategies are introduced.

**Notebook:** `CMPE_258_Assignment4_Colab1.ipynb`

---

### Colab 2 – Monte Carlo Dropout, Initialization, Custom Dropout, and Custom Regularization
This notebook builds on the regularization theme and focuses more specifically on:
- Monte Carlo dropout
- initializer comparison
- custom dropout
- custom regularization
- TensorFlow and PyTorch comparisons

I implemented custom dropout and custom regularization in TensorFlow, compared multiple initialization methods, and also ran similar experiments in PyTorch using built-in and custom components.

This notebook helped me understand that initialization and dropout design can directly affect both convergence and uncertainty estimation.

**Notebook:** `CMPE_258_Assignment4_Colab2.ipynb`

---

### Colab 3 – Callbacks, TensorBoard, Learning Rate Scheduling, and Keras Tuner
This notebook focuses on training workflow tools in TensorFlow.

Main ideas covered:
- EarlyStopping
- ModelCheckpoint
- ReduceLROnPlateau
- TensorBoard
- custom learning rate scheduling
- Keras Tuner
- comparison against a baseline model

The goal here was to study how training can be improved not only through architecture changes, but also through better monitoring, scheduling, and hyperparameter tuning.

**Notebook:** `CMPE_258_Assignment4_Colab3.ipynb`

---

### Colab 4 – Image Augmentation with Keras and KerasCV
This notebook focuses on image augmentation and image classification using the image subset of the Student Wellness dataset.

Main ideas covered:
- baseline image classification
- standard Keras augmentation layers
- KerasCV augmentation layers
- visualization of augmented image samples
- A/B comparison of baseline vs augmented training

This notebook shows how augmentation helps improve generalization by increasing variability in the training distribution.

**Notebook:** `CMPE_258_Assignment4_Colab4.ipynb`

---

### Colab 5 – Text Augmentation and Text Classification
This notebook focuses on text augmentation using the text subset of the Student Wellness dataset.

Main ideas covered:
- text classification baseline
- custom text augmentation
- NLPAug-based augmentation
- comparison of baseline vs augmented training

This notebook was useful for exploring augmentation outside of computer vision and applying it to NLP classification tasks.

**Notebook:** `CMPE_258_Assignment4_Colab5.ipynb`

---

### Colab 6 – Tabular and Time Series Augmentation
This notebook covers augmentation for structured numeric data and sequential data.

Main ideas covered:
- tabular classification baseline
- tabular data augmentation using Gaussian noise
- time series classification baseline
- time series augmentation using jitter/noise
- A/B comparison of baseline vs augmented training

This notebook shows that augmentation techniques can also be applied to non-image data types in a meaningful way.

**Notebook:** `CMPE_258_Assignment4_Colab6.ipynb`

---

# Part 2 – Advanced Deep Learning Constructs
**Covered in Colabs 7–11**

### Colab 7 – Custom Loss, Activation, Initializer, Regularizer, Constraint, and Metric
This notebook focuses on custom TensorFlow/Keras components.

Main ideas covered:
- custom activation function
- custom initializer
- custom regularizer
- custom kernel weight constraint
- custom loss function
- custom metric
- comparison against a baseline model

This notebook helped me understand how much flexibility TensorFlow provides for defining custom behavior in different parts of the training pipeline.

**Notebook:** `CMPE_258_Assignment4_Colab7.ipynb`

---

### Colab 8 – Custom Layers and Custom Model
This notebook focuses on building reusable custom layers and a custom model architecture.

Main ideas covered:
- custom dense layer
- custom Gaussian noise layer
- custom normalization layer
- residual block design
- custom subclassed model
- comparison against a baseline model

This notebook helped me move from customizing individual functions to building a more modular custom architecture.

**Notebook:** `CMPE_258_Assignment4_Colab8.ipynb`

---

### Colab 9 – Custom Training Loops in TensorFlow and PyTorch
This notebook focuses on low-level training control in both TensorFlow and PyTorch.

Main ideas covered:
- TensorFlow custom training loop with `GradientTape`
- PyTorch custom training loop with manual forward/backward/update steps
- manual tracking of training and validation performance
- comparison between TensorFlow and PyTorch custom loops

This notebook was especially useful for understanding what the frameworks are doing behind high-level APIs like `model.fit()`.

**Notebook:** `CMPE_258_Assignment4_Colab9.ipynb`

---

### Colab 10 – Learning Rate Schedulers and Optimizer Comparison
This notebook focuses on optimizer behavior and learning rate strategies.

Main ideas covered:
- fixed learning rate baseline
- step decay
- exponential decay
- cosine decay
- one-cycle style scheduling
- PyTorch optimizer comparison using Adam, SGD with momentum, and RMSprop

This notebook helped me study training dynamics and the effect of optimization strategy on final model performance.

**Notebook:** `CMPE_258_Assignment4_Colab10.ipynb`

---

### Colab 11 – Weights & Biases Experiment Tracking
This notebook focuses on experiment tracking and run comparison.

Main ideas covered:
- training multiple experiments with different hyperparameters
- logging metrics with Weights & Biases
- comparing runs by validation and test performance
- tracking model behavior more systematically

This notebook helped me understand the practical importance of experiment management when multiple training runs are involved.

**Notebook:** `CMPE_258_Assignment4_Colab11.ipynb`

---

# Dataset Used

For this assignment, I used a synthetic multimodal dataset family called the **Student Wellness dataset**.  
It contains multiple subsets designed to support different deep learning experiments:

- **Images** for image classification and augmentation
- **Text** for NLP augmentation and text classification
- **Tabular data** for structured data experiments
- **Time series data** for sequential classification tasks

This common dataset design made it easier to keep the assignment coherent across all 11 notebooks.

---

# Main Technical Themes Covered

Across these 11 Colabs, the assignment covers the following technical areas:

- regularization
- generalization
- dropout
- Monte Carlo dropout
- initialization strategies
- batch normalization
- callbacks
- TensorBoard
- Keras Tuner
- KerasCV
- image augmentation
- text augmentation
- tabular augmentation
- time series augmentation
- custom activation functions
- custom initializers
- custom regularizers
- custom constraints
- custom losses
- custom metrics
- custom layers
- custom models
- custom training loops
- learning rate scheduling
- optimizer comparison
- experiment tracking with Weights & Biases

---

# How to Run

1. Open a notebook in **Google Colab**
2. Mount Google Drive if needed
3. Make sure the Student Wellness dataset folder is available at the expected path
4. Install any notebook-specific libraries such as:
   - `keras-cv`
   - `keras-tuner`
   - `nlpaug`
   - `wandb`
5. Run all cells in order

---

# Submission Notes

- All notebooks were executed and saved with outputs
- The notebooks are organized into Part 1 and Part 2
- Each notebook is accompanied by a video walkthrough
- The videos explain the main code sections, experiments, and outputs

---

# Files in this Repository

- `CMPE_258_Assignment4_Colab1.ipynb`
- `CMPE_258_Assignment4_Colab2.ipynb`
- `CMPE_258_Assignment4_Colab3.ipynb`
- `CMPE_258_Assignment4_Colab4.ipynb`
- `CMPE_258_Assignment4_Colab5.ipynb`
- `CMPE_258_Assignment4_Colab6.ipynb`
- `CMPE_258_Assignment4_Colab7.ipynb`
- `CMPE_258_Assignment4_Colab8.ipynb`
- `CMPE_258_Assignment4_Colab9.ipynb`
- `CMPE_258_Assignment4_Colab10.ipynb`
- `CMPE_258_Assignment4_Colab11.ipynb`

---

# Video Walkthrough Links

- **Colab 1:** Add link here
- **Colab 2:** Add link here
- **Colab 3:** Add link here
- **Colab 4:** Add link here
- **Colab 5:** Add link here
- **Colab 6:** Add link here
- **Colab 7:** Add link here
- **Colab 8:** Add link here
- **Colab 9:** Add link here
- **Colab 10:** Add link here
- **Colab 11:** Add link here

---

# Author
**Nikita Memane**

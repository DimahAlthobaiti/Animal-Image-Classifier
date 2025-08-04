# Animal Image Classifier

This project is a simple image classification model trained to recognize 3 types of animals: **Cat**, **Dog**, and **Hamster**.

## Development Environment

This project was developed and executed using:

- **Google Colab** as the main coding platform
- **Python 3** as the programming language
- **TensorFlow 2.12.1** for model loading and prediction
- **Teachable Machine** for model training and export

## Model Information
- Framework: TensorFlow + Keras
- Classes: `Cat`, `Dog`, `Hamster`
- Format: `keras_model.h5` (Exported from Teachable Machine)

## Requirements
- Python 
- TensorFlow version 2.12.1
- Keras
- A sample image
- keras_model.h5
- Pillow (for image handling)
- NumPy

## How to Use

Follow these steps to run the model and classify an image:

### 1. Install Required Libraries

Make sure to install **TensorFlow 2.12.1** before anything else:
<pre> !pip install tensorflow==2.12.1 </pre>

### 2. Load the Model and Labels
Make sure these two files exist:

keras_model.h5 → the trained model file

labels.txt → the list of class names (e.g., Cat, Dog, Hamster)

### 3. Upload or Choose a Sample Image
Upload your own image (make sure it's a clear image of an animal from one of the classes)

### 4. Image Preprocessing (done automatically)
Once the image is loaded:

It's resized to 224x224 pixels (to match the model's input size).

It's converted to a NumPy array.

It's normalized to fit the range [-1, 1] which is required by the model.

### 5. Make a Prediction
The preprocessed image is passed into the model through: 
prediction = model.predict(data)

The model returns a confidence score for each class. The class with the highest score is selected using:
index = np.argmax(prediction)

### 6. View the Results
The code then prints:

The predicted class name (e.g., Dog)

The confidence score (e.g., 0.999 means 99.9% confident)

## Examples: 
![CodeSample1](https://github.com/user-attachments/assets/63d9f823-2ce7-4753-9bb1-adb10041248c)
![CodeSample3](https://github.com/user-attachments/assets/fa287b74-7fa2-4639-a288-f68a8a6ff977)
![CodeSample2](https://github.com/user-attachments/assets/b88bf03d-3747-4cdc-a47e-b2c9e00ed810)

## Results from using Teachable machine 

![SecSampleDone](https://github.com/user-attachments/assets/bb4631e9-c680-4eda-b53c-44a23b2d783c)
![FirstSampleDone](https://github.com/user-attachments/assets/1512ee3f-9860-4b9b-afc9-fb7e3f50fc3a)
![ThirdSampleDone](https://github.com/user-attachments/assets/80175fd2-f7cc-4fa9-80b1-d9ba5478746b)




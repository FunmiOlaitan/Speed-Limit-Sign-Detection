# Speed Limit Sign Detection using Convolutional Neural Networks (CNN)

Speed limit signs are important for promoting safe driving practices, providing drivers with information about road conditions, and enforcing traffic laws. By indicating the maximum speed at which vehicles should travel on a particular road, these signs can help to reduce the likelihood of accidents caused by excessive speed. 

Machine learning can be utilised to recognise road signs, using computer vision algorithms trained on large datasets of labelled images. These algorithms allow machines to accurately identify different types of road signs, improving road safety and enhancing autonomous driving systems. 
## Description
This project implements a Convolutional Neural Network (CNN) model for detecting Speed Limit signs from images. The CNN is trained on a dataset containing images of Speed Limit signs and non-Speed Limit images. After training, the model can accurately classify new images as either having a Speed Limit sign or not, making it useful for various real-world applications, including traffic sign recognition systems and road safety enhancement.

## Dataset Directory Structure
Ensure the dataset is organised in the following directory structure:
```
C:/Users/funmi/GitRepositories/Speed-Limit-Sign-Detection/Roadsignfile
    ├── train
    │   ├── Speed_Limit_20
    │   ├── Speed_Limit_30
    │   ├── Speed_Limit_50
    │   └── ...
    ├── test
    │   ├── Speed_Limit_20
    │   ├── Speed_Limit_30
    │   ├── Speed_Limit_50
    │   └── ...
    └── val
        ├── Speed_Limit_20
        ├── Speed_Limit_30
        ├── Speed_Limit_50
        └── ...
```
## Splitting Dataset
To split the dataset, you can use the `Splitting Dataset.ipynb` notebook. This notebook uses the `splitfolders` library to split the dataset into train, validation, and test sets with specified ratios. The resulting split datasets will be saved in the folder `"C:/Users/funmi/Documents/Roadsignfile"` and the file `"Roadsignfile"` was copy and pasted into my repository's file path. You can also save the split datasets directly into your repository.

## Usage
Follow these steps to use the provided code and train your own Speed Limit sign detection model:

1. **Install Required Libraries:** Before getting started, ensure you have the necessary libraries installed. Open a terminal or command prompt and run the following command to install the required packages:

```bash
pip install tensorflow keras scikit-image
```

2. **Dataset Preparation:** Organise your dataset according to the specified [Dataset Directory Structure](#dataset-directory-structure). Create separate folders for training, testing, and validation data, each containing images of Speed Limit signs in their respective subfolders.

3. **Training the Model:** Open the `Classifying Speed Limit Signs.ipynb` notebook to implement and train the CNN model. The notebook will perform the following steps:

   - Load the dataset and print folder names and the number of categories detected.
   - Augment the training data and set up data generators for training, validation, and testing.
   - Build the CNN model with the specified architecture.
   - Train the model and visualise its accuracy and loss during training.
   - Evaluate the model's performance on the test dataset.
   - Save the trained model as "model.h5".
   - Test the model on new images and classify them as having a Speed Limit sign or not.

4. **Inference on New Images:** The trained model can be used to make predictions on new images containing Speed Limit signs. Use the `classifier()` function in the `Classifying Speed Limit Signs.ipynb` notebook. Provide the file path of the image as an argument to the function.

   Example usage:
   ```python
   classifier("C:/Users/funmi/GitRepositories/Speed-Limit-Sign-Detection/RoadSign.jpg")
   classifier("C:/Users/funmi/GitRepositories/Speed-Limit-Sign-Detection/NotRoadSign.jpg")
   ```
## Acknowledgements
Special thanks to the creators of the `splitfolders` library for simplifying dataset splitting and to the authors of the various libraries used in this project.

## Support
For any issues or inquiries, feel free to open an issue in the repository. Your contributions and feedback are welcome to enhance the project further.
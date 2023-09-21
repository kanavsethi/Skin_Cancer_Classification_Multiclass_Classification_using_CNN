# Skin Cancer Detection - Multiclass Classification using CNN 🩺📸

## Problem Statement 📜

Detecting skin cancer, particularly melanoma, is a critical task in the medical field. Melanoma accounts for 75% of skin cancer deaths and early detection is crucial for successful treatment. This project aims to build a Convolutional Neural Network (CNN) model that can accurately detect skin cancer from images, helping dermatologists identify potential cases more efficiently and reducing the need for manual diagnosis.

## Approach 🛠️

We use TensorFlow to build the CNN model and leverage data augmentation techniques to address overfitting. Augmentation helps create variations of the training images, making the model more robust and capable of generalizing to unseen data. We use Tensorflow Augmentation as well as the Augmentor Python package is used for image augmentation.

## Model Architecture 🏗️

The CNN model has the following structure:

```
Model: "Model With Augmented Images Input"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 Input_Rescaling (Rescaling)  (None, 180, 180, 3)      0         
                                                                 
 Conv2DH-1 (Conv2D)          (None, 180, 180, 16)      448       
                                                                 
 MaxPoolH-1 (MaxPooling2D)   (None, 90, 90, 16)        0         
                                                                 
 Conv2DH-2 (Conv2D)          (None, 90, 90, 32)        4640      
                                                                 
 MaxPoolH-2 (MaxPooling2D)   (None, 45, 45, 32)        0         
                                                                 
 Conv2DH-3 (Conv2D)          (None, 45, 45, 64)        18496     
                                                                 
 MaxPoolH-3 (MaxPooling2D)   (None, 22, 22, 64)        0         
                                                                 
 Flatten-5 (Flatten)         (None, 30976)             0         
                                                                 
 DenseH-6 (Dense)            (None, 128)               3965056   
                                                                 
 DropOut-4 (Dropout)         (None, 128)               0         
                                                                 
 Output (Dense)              (None, 9)                 1161      
                                                                 
=================================================================
Total params: 3,989,801
Trainable params: 3,989,801
Non-trainable params: 0
_________________________________________________________________
```

## File Structure 📂

- `Skin Cancer Classifier.ipynb`: Jupyter notebook for training the skin cancer classifier.
- `Augmented Image Cleaner.ipynb`: A notebook to delete images created using augmentation to return the project to its original state.
- `Data/Train/{Class_Name}/*.jpg`: Training images, organized by class.
- `Data/Test/{Class_Name}/*.jpg`: Testing images, organized by class.

## Getting Started 🚀

1. Clone this repository to your local machine.
2. Install the necessary dependencies (TensorFlow, Augmentor, etc.).
3. Open and run the `Skin Cancer Classifier.ipynb` notebook to train the skin cancer detection model.
4. Explore the results, evaluate the model's performance, and make improvements as needed.
5. Incase you need to clear up images created by Augmentor Package, Run `Augmented Image Cleaner.ipynb`.

## Usage 🤖

Once trained, this model can be used to classify skin cancer images into different classes, helping in the early detection and diagnosis of melanoma and other skin conditions.

## Contributing 🤝

Contributions are welcome! Feel free to open issues, submit pull requests, or provide feedback on how to improve this skin cancer detection project.

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

If you have any questions or feedback, please don't hesitate to reach out.

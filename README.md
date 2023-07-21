# ResNet50 Image Classification with TensorFlow

This repository contains code for building an image classification model using the ResNet50 architecture with TensorFlow. The model is trained on a custom dataset containing images of rice, categorized into different classes.

## Dataset

The dataset used for training, validation, and testing is stored in the `Rice_Image_Dataset` folder. It consists of images of rice with different varieties and qualities. The dataset is divided into three subsets:

- **Train**: This folder contains the training set images used to train the ResNet50 model.
- **Val**: The validation set images, used to monitor the model's performance during training.
- **Test**: The test set images, used to evaluate the trained model's accuracy on unseen data.

## Dependencies

To run the code in this repository, you will need the following dependencies:

- TensorFlow 2.x
- Matplotlib
- split-folders

You can install these dependencies using the following command:
 
 ```bash
pip install tensorflow matplotlib split-folders
 ```

Update the dataset path in the code to your dataset's path:

```python
# Update these paths to your actual dataset paths
train_data = train_datagen.flow_from_directory(
    '/path/to/your/train',
    target_size=(256, 256),
    batch_size=32
)

val_data = val_datagen.flow_from_directory(
    '/path/to/your/val',
    target_size=(256, 256),
    batch_size=32
)

test_data = test_datagen.flow_from_directory(
    '/path/to/your/test',
    target_size=(256, 256),
    batch_size=32
)
```
## Result

The provided code will train a custom ResNet50 model using transfer learning, fine-tuning it for rice image classification, and display accuracy and loss plots during the training process.

## License

This project is licensed under the MIT License

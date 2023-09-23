### Casting_Defect_Detection

LINK: https://universe.roboflow.com/casting-defects/cast-defect-w5mh1
## Defected Object  Classification in Casted Metal Parts with MobileNet V2

This project aims to classify casted objects as either defected or non-defected using the MobileNet V2 model pre-trained on the ImageNet dataset. MobileNet V2 is a deep neural network architecture developed by Google that has shown excellent performance in various computer vision tasks.

### Overview
The primary goal of this project is to leverage transfer learning by utilizing a pre-trained MobileNet V2 model as a feature extractor. Transfer learning allows us to benefit from the knowledge learned by MobileNet V2 on a diverse set of image data from ImageNet. We then fine-tune the model to adapt it to our specific task of classifying defected and non-defected casted objects.

### Project Structure
The project is structured as follows:

Data Preparation: Collect and preprocess a dataset of casted objects, separating them into two classes: defected and non-defected.
![image](https://github.com/SejalWasule/Casting_Defect_Detection/assets/102143995/578ec5b7-7d90-42c4-a6b2-de397d05e783)

Model Building:

Instantiate a MobileNet V2 model pre-loaded with ImageNet weights, excluding the classification layers.
Add a Global Average Pooling 2D layer to convert the features into a single vector per image.
Add a Dense layer with a single output unit for binary classification.
Model Compilation: Compile the model with the appropriate loss function and optimizer for binary classification.

### Training:

Train the model initially for a specified number of epochs.
Monitor training progress, including loss and accuracy.
Model Saving: Save the trained model to an HDF5 file for later use.

 Learning Curves Visualization: Visualize training and validation accuracy/loss curves to assess model performance.
 ![image](https://github.com/SejalWasule/Casting_Defect_Detection/assets/102143995/1e9ca66a-339c-421d-9cee-f17912c2c10f)


### Fine-Tuning:

Optionally, fine-tune the top layers of the pre-trained MobileNet V2 model to further improve classification performance.
Fine-tuning allows the model to adapt to the specific characteristics of the casted objects dataset.
Getting Started
To get started with this project, follow these steps:

Clone this repository to your local machine.

Prepare your dataset of casted objects, ensuring it follows the directory structure and labeling conventions specified in the data preparation section.

Run the provided code to build, train, and evaluate the model. You can adjust hyperparameters as needed.

Optionally, experiment with fine-tuning to improve model performance on your specific dataset.

### Results
Model performance: Training: loss: 0.0020 - accuracy: 0.9995 
                   Validation: loss: 0.0277 - accuracy: 0.9966
                   Test: loss: 0.0429 - accuracy: 0.9945
After training, the model is expected to achieve high accuracy in classifying defected and non-defected casted objects. You can evaluate the model's performance on new data and use it for real-world applications.

### License
This project is licensed under the MIT License, which means you are free to use, modify, and distribute the code for both personal and commercial purposes.

Feel free to contribute to this project by opening issues or pull requests if you have any suggestions or improvements.

If you have any questions or need further assistance, please don't hesitate to contact us.

Happy coding!







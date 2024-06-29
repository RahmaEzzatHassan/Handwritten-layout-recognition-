## Fine Tunning
### 1- Label Definition 
Define the labels for document layout elements:
Figure
Headline
None
Subtitle
### 2- Paths to Dataset 
Specify the paths to your training and validation datasets:
train_path: Path to the training dataset images.
val_path: Path to the validation dataset images.
### 3- YAML Configuration 
Create a YAML configuration file for the dataset:
The data_dict dictionary contains paths to the training and validation datasets, the number of classes (nc), and the names of the classes.
Save this configuration to a YAML file named your_data.yaml.
### 4- Load Pre-trained Model
Load a pre-trained YOLOv8x model from a specified file path.
### 5- Fine-Tuning the Model 
Replacing the final classification layer to match the number of classes in the custom dataset.
Training the model for [70] epochs using a learning rate of [0.001] and a batch size of [14].
Applying data augmentation techniques such as Brightness, rotation, and flip to improve model generalization.
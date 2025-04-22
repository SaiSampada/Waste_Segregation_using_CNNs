# Waste_Segregation_using_CNNs

Overview:
This project uses a Convolutional Neural Network (CNN) to classify waste images into 7 categories:
Cardboard
Food_Waste
Glass
Metal
Other
Paper
Plastic

Dataset:
Over 7,000 images
Organized into 7 folders (one per class)

Preprocessing:
All images resized to 128x128 pixels
Images converted to RGB and normalized (pixel values scaled to [0, 1])
Labels encoded using LabelEncoder

Dataset split into 70% training and 30% validation
Verified image sizes and class distributions

Model Architecture:
3 convolutional layers with ReLU activation
Each followed by BatchNormalization, MaxPooling, and Dropout
Flatten layer
Dense layer with 128 units and ReLU
Final Dense layer with softmax for 7 classes
Dropouts are used to prevent overfitting

Training Details:
Loss function: Sparse Categorical Crossentropy
Optimizer: Adam (learning rate 0.0001)
Trained for 20 epochs
Validation accuracy reached 64.5%

Data Augmentation:
Rotation, width/height shift, zoom, and horizontal flip used
Helped increase variety and improve generalization

Observations:
Model showed improvement by tuning hyperparameters 
Validation accuracy improved slightly with augmentation

Conclusion:
Basic CNN custom model was successfully trained for waste classification
Data augmentation and dropout helped control overfitting
Further improvements can be made with better architecture or tuning

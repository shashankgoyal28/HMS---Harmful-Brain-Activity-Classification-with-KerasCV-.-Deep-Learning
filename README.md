# HMS---Harmful-Brain-Activity-Classification-with-KerasCV-.-Deep-Learning
Training and Inferring Deep Learning Models on EEG Data with KerasCV

This notebook provides a step-by-step guide on training and inferring a Deep Learning model to classify patterns in EEG data. We utilize a variety of pre-trained models, including EfficientNetV2, ResNet50_v2, MobileNet_v3_large, and DenseNet201, leveraging their strengths to achieve optimal performance. Additionally, we enhance our model by concatenating it with a 1D WaveNet model to capture temporal dependencies in the EEG data.

Models and Their Accuracies

EfficientNetV2: Achieves an accuracy of 0.70.
ResNet50_v2: Achieves an accuracy of 0.63.
MobileNet_v3_large: Achieves an accuracy of 0.63.
DenseNet201: Achieves an accuracy of 0.67.


Data Preparation

The dataset used in this notebook consists of EEG data, which we convert into spectrograms to facilitate pattern classification. The spectrograms provide a visual representation of the frequency spectrum of the EEG signals, allowing the models to learn and identify distinct patterns.

Model Architecture

Pre-trained Models
EfficientNetV2: Known for its efficiency and accuracy, it serves as a robust baseline.
ResNet50_v2: Utilizes residual connections to mitigate the vanishing gradient problem, improving training depth.
MobileNet_v3_large: Balances accuracy and computational efficiency, making it suitable for mobile applications.
DenseNet201: Connects each layer to every other layer, enhancing gradient flow and feature reuse.
1D WaveNet Model
To complement the pre-trained models, we introduce a 1D WaveNet model. WaveNet, originally developed for audio synthesis, is adept at modeling sequential data. By concatenating this model with the spectrogram-based models, we capture both the temporal and frequency-based features of the EEG data.

Training and Inference

Data Augmentation: We apply data augmentation techniques to the spectrograms to increase the diversity of the training dataset and improve model robustness.
Model Training: The models are trained using KerasCV, optimizing for accuracy through various hyperparameter tuning and training strategies.
Model Concatenation: The outputs of the spectrogram-based models are concatenated with the 1D WaveNet model, creating a comprehensive model that leverages both types of features.
Evaluation: The model is evaluated on a validation set to assess its performance. We report the accuracies of the individual models and the concatenated model to highlight the improvements achieved.
Conclusion

This notebook demonstrates an effective approach to classifying EEG patterns using a combination of pre-trained models and a 1D WaveNet model. By leveraging KerasCV and advanced data augmentation techniques, we achieve competitive accuracies, showcasing the potential of this methodology for EEG data analysis.

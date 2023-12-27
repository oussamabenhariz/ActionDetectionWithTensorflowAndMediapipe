# ActionDetectionWithTensorflowAndMediapipe
## 1. Install Dependencies:

Ensures necessary libraries are installed for tasks like mediapipe, model training, and visualization.
## 2. Import Dependencies:

Imports required libraries for mediapipe model access, image processing, data manipulation, model creation, and evaluation.
## 3. Extract Keypoint Values:

Defines functions to extract and store keypoints for pose, face, and hands from mediapipe results.\
Combines all keypoints into a single array for later use.
## 4. Setup Folders for Collection:

Creates a directory structure to organize collected keypoint data for different actions.
## 5. Collect Keypoint Values for Training and Testing:

Captures videos with mediapipe, extracts keypoints for each frame, and saves them as NumPy arrays.\
Loops through actions and sequences for comprehensive data collection.
## 6. Preprocess Data and Create Labels and Features:

Loads collected keypoints data back into arrays.\
Assigns categorical labels to each action for model training.\
Prepares features (keypoint data) and labels for model training and testing.
## 7. Build and Train LSTM Neural Network:

Sets up TensorBoard for visualizing training progress.\
Defines a model checkpoint callback to save the best model during training.\
Constructs an LSTM neural network architecture suitable for sequential data.\
Compiles the model with appropriate optimizer and loss function.\
Trains the model using the prepared features and labels.
## 8. Load the best Model:

Loads the best model weights (saved during training) for later prediction.
## 9. Make Predictions:

Uses the trained model to make predictions on the test set.\
Compares predicted actions with true labels for evaluation.
## 10. Evaluation using Confusion Matrix and Accuracy:

Calculates a confusion matrix to visualize model performance across different actions.\
Computes overall accuracy to measure its prediction correctness.
## 11. Test in Real Time:

Sets up variables for real-time prediction.\
Defines a function to visualize prediction probabilities on a video frame.\
Opens the webcam and continuously performs model prediction on captured frames.\
Displays prediction results and keypoints on the video for visual feedback.
## Key Points:
The code effectively demonstrates how to use MediaPipe for human pose estimation and build an LSTM model for action recognition.\
It covers data collection, preprocessing, model training, evaluation, and real-time prediction.\
It includes helpful visualizations for both model training and real-time prediction.\
The code is well-structured and easy to follow, making it a valuable resource for learning and experimenting with action recognition.

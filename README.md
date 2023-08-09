# Real-Time-Sign-Language-Detection

This project showcases a straightforward hand gesture recognition system using Python, OpenCV, and MediaPipe. It involves data collection, processing, model training, and real-time detection. The webcam captures diverse hand gestures, classified into three categories with 50 images each, stored under "./data/1" for class 1, and so on.

In data processing, MediaPipe's hand-tracking module extracts x and y coordinates of 21 hand landmarks, normalizing them through min-max normalization. These normalized landmarks form 1D arrays stored alongside class labels in a numpy array.

Model training employs scikit-learn's RandomForestClassifier, assessing accuracy on a test set. For real-time detection, the webcam captures frames, extracting normalized landmarks with MediaPipe, and predicting gesture classes using the trained random forest model. Results display in the frame, along with landmark visualizations. Users exit using the 'X' key.

# Assignment-4.1-Mood-Detection-with-OpenCV

Introduction & Instruction

As an introduction to computer vision, you are to perform the simple task of mood detection. Mood detection is the process of identifying and understanding a person's current emotional state. It can be done through a variety of methods, but we will focus on Facial expression recognition. Facial expressions are one of the most important cues for understanding human emotions. Mood detection systems can use computer vision techniques to analyze facial features and identify specific expressions, such as happiness, sadness, anger, you must attain the following objectives:

- Recognize when a face is yours or not.
- Recognize only your mood (happy, sad, angry, or confused).
- Perform testing to show the performance of your implementation.

### Steps taken in this Activity
1. Face Recognition Setup Using DeepFace \
   Used the DeepFace library to verify if the detected face belongs to me.
   - Installed deepface using pip.
   - Used my reference image
   - During the webcam detection every detected face is compared to my reference image
   - If the verification is True, then it is my face, otherwise it's someone else.

2. Prepared a Custom Facial Expression Dataset \
   Created a folder called custom_facial_expression_dataset, with subfolders:
   - train/, validation/, test/
   - Inside each folder: anger/, happy/, sad/, surprise/, others/

3. Used ImageDataGenerator to Load and Augment Images \
   Used TensorFlow's ImageDataGenerator to:
   - Load images by folder
   - Normalize the pixel values
   - Apply data augmentation

4. Used a Pre-Trained Model VGG16 to create Mood Detection Model \
   Used transfer learning with VGG16

5. Trained the Model
   Compiled the model using:
   - Adam optimizer
   - Categorical crossentropy for multi-class classification
   - EarlyStopping to avoid overfitting

6. Saved the Trained Model \
   After training I saved the model so it can be used later

7. Testing of Facial Recognition + Mood Detection (Real-Time Webcam) \
   Used OpenCV to access the webcam and detect faces, then used DeepFace to check if the detected face is my face, then if it is my face, the face is passed to the trained MobileNetV2 to predict my mood and display the result.

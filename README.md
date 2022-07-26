# face_recognition
MATLAB GUI to perform facial recognition

Before using the GUI add two empty folders to the MATLAB path, one titled "Database" and a second folder titled "Image". These folders are needed to store the users in the database as well as to store temporary images needed for the app to function properly. 

Prior to using the app ensure you have the following add-ons installed on your version of MATLAB: 
- USB Webcam Add-on
- Computer Vision Toolbox 
- Statistics and machine learning toolbox

The app registers users in the database by taking six photos of each user. Faces are recognized in the photo using the computer vision toolbox. If a face is not detected it will automatically retake the photo. If a background object is detected as a face, the photo can be re-taken using the dropdown menu. 

The facial recognition works by taking a photo and again recognizing a face within the photo using the computer vision toolbox. If no face is detected the user is prompted to re-try by clicking the facial recognition button again. If a face is detected, the facial features are compared to the faces in the database using HOG feature extraction. If a match is found (w/in an error of 0.3), the app prints "Hello name". If no match is found the app prints "No user found". 

The webcam is default set to a USB webcam, if you are using a different computer you may need to manually change these lines of code to set your webcam object to match your webcam. 

The minimum face detection size is set to 50x50 pixels. If you find that background objects are being picked up too frequently you can increase this size. If you find that no face is being detected too frequently you can decrease this size. 

The minimum error for a match is set to 0.3. This can be adjusted manually in the code. 

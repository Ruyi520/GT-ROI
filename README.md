# Attention-detector with ROI

This project consist of several modules all implemented in an GazeClassifier.ipynb file. 
Our approach of pervasive attention tracking with respect to an region of interest(ROI) encompasses a heirachical implementation of computer vision algorithms in the same notebook file. (Note: Performance is dependent on system specifications and installation dependencies.

Our objective is to compute the sum vector of pitch, row and yaw values of faces as well as the pitch and yaw angles of the eyes (average) which is relative to the distance vector of the point to the image plane. The image frames of detected faces, eyes are parsed through our covnet architecture( using a pretrained VGG16 model) is simply used to classify the real-time gaze directions.

Given user-defined real world properties of an environment like camera intrisic and extrinsic properties.
We show a model which estimates the X, Y, Z point coordinates of known u,v points on our image plane. The derived X, Y, Z point coordinate is used to determine an Optimal gaze angle which static relative to centre of board(ROI). This is compared to the Total gaze vector from the face and eyes.



# Attention-detector with ROI

This project consist of several modules all implemented in the GazeClassifier.ipynb file. 

Our approach of pervasive attention tracking with respect to a region of interest(ROI) encompasses a heirachical implementation of computer vision algorithms in a single notebook file. (Note: Performance is dependent on system specifications and installation dependencies i.e requirements.txt)

Our objective is to compute the Total Gaze Vectors(TGV) derived from the vector sum of pitch, row and yaw values of faces (1 X 3 dimension) and the pitch and yaw angles of the eyes (average of both eyes i.e 1 X 2 dimension).

Given some user-defined properties of the real world environment such as classroom dimensions(including the ground and wall plane), camera intrisic and extrinsic properties. We show a model which estimates the X, Y, Z point coordinate from the known u,v point the of face detected on our image plane. 


A static Optimal Gaze Angles/Vector (OGV preferred) is derived from the object's X, Y, Z point coordinate which is relative to centre of board(ROI). We compare the TGV and the OGV to determine the Gaze delta over time or over n number of frames.

This product is relative to the distance vector of the point to the image plane. The image frames of detected faces, eyes are parsed through our covnet architecture( using a pretrained VGG16 model) is simply used to classify the real-time gaze directions.



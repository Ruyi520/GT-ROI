# Gaze Estimation with a specified Region of Interest (ROI)

This project consist of several modules implemented in the GazeClassifier.ipynb and EyeGazeClassifier.ipynb file.

We approach the problem of gaze tracking with respect to a region of interest(ROI) to encompass a heirachical implementation of computer vision algorithms in a single notebook file. (Note: Performance is dependent on system specifications and installation dependencies i.e requirements.txt)

Our objective is to compute the Total Gaze Vectors(TGV) derived from the summing the gaze vector (pitch, row and yaw values : 1 X 3 dimension) of a face and the eye gaze vector(pitch and yaw angles i.e average of both eyes, 1 X 2 dimension).

  Total Gaze Vector(TGV): Θh, Θv = (Px + Ex, Py + Ey)
  
  where Θh is the horizontal component of TGV.
        Θv is the vertical component of TGV.
        Px, Py is the 2D head pose.
        Ex, Ey is the 2D eye_gaze.
        
        Note: Pz represents the 3-axis of the head-pose (eye alignment). This value is used to align eye images
        before parsed to the classifier.

The subject's real-world position (X, Y, Z) and the center coordinate of ROI(board) is used to derive an Optimal Gaze Angles/Vector (OGV). The OGV is simply a function of the subject's position relative to the center position of the ROI. We compare the TGV and OGV to determine the Gaze delta(gaze deviation) over time or over N number of frames.

Given some user-defined properties of the reaoll world environment such as classroom dimensions(including the ground and wall planes), camera intrisic and extrinsic properties. We show some projection transformation techniques used to estimates the (X, Y, Z) point coordinate from a known point (u,v) of a face detected on the image plane.

This product is relative to the distance vector of the point to the image plane. The image frames of detected faces, eyes are parsed through our covnet architecture( using a pretrained VGG16 model) is simply used to classify the real-time gaze directions.



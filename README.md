# Basic-Motion-Detection
Detects motion in a video stream. If the motion sustains for a larger period of the time and is large enough it reports that the motion is detected.

# Dependencies

    OpenCV 2
    Image Utilities (imutils)

# Working Theory

OpenCV is used to calculate absolute frame deltas against the most recent saved frame and the current frame. The frame deltas are then passed through a threshold filter, and bounding boxes are drawn around contours of the thresholded frame. (The frequency of saving frames is determined via the user parameter.)

A sufficiently large bounding box derived from the contours of a thresholded frame delta image is considered movement.

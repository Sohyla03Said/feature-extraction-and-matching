# feature-extraction-and-matching
This project demonstrates how to detect and locate a specific object within a target image using SIFT (Scale-Invariant Feature Transform), FLANN-based feature matching, and Homography transformation. The result is a bounding polygon drawn on the target image, highlighting the detected object.

# Technologies Used
 . Python 
 . OpenCV (cv2)
 . NumPy
 . Matplotlib

# How It Works
-> Read Input Images:
   The query image (object to detect) is read in grayscale.
   The target image (where we search for the object) is read in color and also converted to grayscale.

-> Feature Detection:
   SIFT is used to detect keypoints and compute descriptors in both images.

-> Feature Matching:
   FLANN (Fast Library for Approximate Nearest Neighbors) is used to match descriptors between the query and target images.

-> Lowe’s Ratio Test:
   Filters out poor matches by comparing distances of nearest neighbors.

-> Homography & Object Localization:
   If enough good matches are found, homography is computed.
   The object corners are transformed using the homography matrix and drawn on the target image.

-> Display Result:
   The target image is displayed with the detected object outlined in green.


# Rectangle-shape 
![Image](https://github.com/user-attachments/assets/31b45cd1-8747-434c-8db5-1edcf9dd6df4)

# Keypoint-match
![Image](https://github.com/user-attachments/assets/85d3e4fb-b167-4f68-8fb9-0b0991b77005)

# Image Alignment using OpenCV
 
There are certain ways to take a large area image. The first of these is to increase the distance, but it is not desired to be preferred because this does not give the desired result. The other is to take a panoramic image that can cover even a 360-degree area. So you can capture a large scene. Panoramic pictures are created by combining several images with overlapping areas. This process is called image stitching. In order to realize this process, the related parts of the pictures must be detected and oriented accordingly. In this study, it is aimed to image stitching and design the necessary steps for this.

# Details of the Approach and Methods Used

First step to creating a panorama is align two images to process. To do this, the keypoints and descriptors must be found. Interesting, distinct features we also call keypoints and those provide us to compare scenes. Descriptors that are part of the keypoints. There are several feature detection algoritms but i used ORB.

Next, detect the matching points for two inputh images. Similary finding process also it can explaining like, it suggests that there are repetitive patterns in your images. Thus, the feature points that are related to each other in the two images, ie where the image matches, are found. I used BFMatcher to do this.

Other process is applying the RANSAC method to estimate homography. Next one is wrapping on one image, while keeping one as reference. One of the photographs is kept as a reference, and the other is extracted using the homogram matrix calculated in the previous step. Thus, the necessary information for the alignment of the pictures is collected. Stitching process is completed at this stage. Finally, a border is prepared in accordance with the created picture and the process is completed.

# Results
![alt text](https://github.com/bakkyn/Image-Alignment-using-OpenCV/blob/main/results/1.png?raw=true)

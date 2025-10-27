Billy Burns
Repository #2
CS391 - Computer Vision

AI Usage... GitHub CoPilot and Perplexity helped to create the boilerplate and more challenging code especially for end of Part 3 
and the majority of Part 4. For part 1 and 2, copilot was used mainly for code completeion for efficency and for boilerplate as well. 

Part 1:
![Detected SIFT Keypoints](images/SIFTPT1Image.png)

The visualization above showcases the SIFT keypoints that were detected and the size of the circle surrounding each keypoint showcases
the size of the blob. The larger the circle around the keypoint, the larger the blob detetcted. These blobs can be specifcially seen 
around edges and other areas of high contrast. However, some errors can be seen within the visualization. The turqoius-ish/blue circles
seen in the grey areas between the white pages show little to no contrast or edegs but contain some of the largest detected blobs. Therefore, 
I beleive that these specific keypoints are errors and should be deleted. 

Part 2:
![Detected SIFT Keypoints](images/SIFTPT2Image.png)

In order to get the largest number of blobs detected, I made sure to not only lower the contrast threshold to 0.02, but I also increased 
edge threshold to 15. This yeilded 270 more keypoints detected than the original untuned detection image. This is due to the fact that by 
reducing the contrast threshold, the SIFT detction needs less contrast within the image to trigger a keypoint detetcion. Additionally, 
by increasing the edge threshold, this allowed the SIFT detection to detect more edge keypoints. Both of these tunes allowed for the SIFT
detection to increase the number of detected keypoints compared to the original SIFT method. 

Part 3:
![Detected SIFT Keypoints](images/SIFTPT3.1Image.png)

A SIFT descriptor is a set of 128 values that helps to showcase an areas edge directions in vector form. This helps to showcase the specific
edges within an image allowing you to track the specific image locations and spots regardless of how the image is transformed. For the area
showcased in the image above, the vectorized values are as follows...

[  8.  16.   2.   8.  25.   7.   0.   0.  32.  26.  18.  53. 122. 122.
   8.   8. 122.  28.   7.   6.  16.  38.  70.  64.  18.   1.   5.  25.
  89.  90.  57.  52.   1.   2.   3.  13.   4.   2.   0.   0.  18.  10.
  12. 122.  90.  65.  12.  11. 122.  45.  10.  22.  13.  17.  12.  49.
  53.  11.  21.   3.  13.  69.  26.  11.   0.   0.   0.   2.   1.   0.
   0.   0.   5.   2.   1.  23.  27.  30.  83.  37.  76.   8.  24.  44.
  48.  19.  75. 122.  20.  18. 122. 115.  33.  16.   6.  11.   0.   0.
   0.   0.   0.   0.   0.   0.   1.   1.   0.   0.   0.   0.   8.   8.
   5.   4.   2.  12.  59.  66.  19.  14.   5.   3.  32.  38.  46. 122.
 122.  58.]

Part 4:
![Detected SIFT Keypoints](images/SIFTPT4Image.png)
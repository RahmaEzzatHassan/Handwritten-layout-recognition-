The main objective is to
identify the interest points in the image which further helps in feature extraction.
Pre-processing performs operations with images at the lowest level of abstraction
where both input and output are intensity images. The goal of pre-processing is to
improve the image data by removing annoying distortions and enhance image
features significant for further processing. Our preprocessing sequence as
following: Gaussian filter, GrayScale, Binarization, Horizontal lines removal, Normalization and Data Augmentation

### Line Segmentation

* If the label of the YOLO box is None, it detects block of text in the image. so we need to apply line segmentation to it.
* Line Segmentation is a technique that chops the block of texts in the image up into horizontal slices .

#### Line Segmentation Steps:

1- Convert image to grayscale: It will convert BGR image to grayscale using cv2.cvtColor.

2- Apply binary inverse thresholding: This applies binary thresholding with inversion to the image using cv2.threshold to create a binary image where foreground objects are white and the background is black.

3- Apply morphological dilation: Morphological dilation is applied to the thresholded image using cv2.morphologyEx to help thicken the foreground objects, potentially connecting slightly broken lines.

4- Contour Detection: Contours are found in the binary mask using cv2.findContours  ,This identifies connected components (contours) in the binary image. Ideally, each line of text would be a separate contour. 

 5- Bounding Box & ROI Extraction: In this step we calculates the bounding rectangle for each contour using cv2.boundingRect, and draws these bounding boxes the image. after that for each bounding box, the ROI is extracted from the original image then each line then pass it to the model .
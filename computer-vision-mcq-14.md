# Part 14

# Computer Vision Quiz: Applications of Image Feature Matching

## Multiple Choice Questions (MCQs)

### Question 1

In image stitching for panorama creation, what is the primary role of SIFT features after detecting keypoints across overlapping regions?

- A) To directly blend pixel intensities between images
- B) To estimate homography transformation between images
- C) To compress the final panoramic image
- D) To remove noise from individual images

**Correct Answer: B**

### Question 2

For copy-move forgery detection, SIFT features help identify manipulated regions by:

- A) Detecting pixel-level inconsistencies in color distribution
- B) Analyzing compression artifacts in JPEG images
- C) Matching features and identifying consistent affine transformations among matches
- D) Computing statistical properties of image histograms

**Correct Answer: C**

### Question 3

In video stabilization using SIFT, what happens after tracking keypoints between frames?

- A) Keypoints are directly used to interpolate missing pixels
- B) Motion model estimation (e.g., affine transform) followed by trajectory smoothing
- C) Frame rate is automatically adjusted based on motion magnitude
- D) Color correction is applied to maintain consistency

**Correct Answer: B**

### Question 4

Which statement best describes the advantage of using SIFT for object recognition compared to template matching?

- A) SIFT is faster for real-time applications
- B) SIFT requires less memory storage
- C) SIFT is robust to scale, viewpoint, and illumination changes
- D) SIFT works only with grayscale images

**Correct Answer: C**

### Question 5

In content-based image retrieval using the Bag-of-Words approach with SIFT features, the voting mechanism works by:

- A) Counting pixel similarities between query and database images
- B) Matching individual SIFT descriptors and accumulating votes for each database image
- C) Comparing global image histograms directly
- D) Using neural networks to classify image categories

**Correct Answer: B**

### Question 6

For medical image registration (CT vs MRI), SIFT features are particularly useful because they:

- A) Can directly convert between different imaging modalities
- B) Enhance image contrast automatically
- C) Detect and match corresponding anatomical features despite different imaging characteristics
- D) Reduce radiation exposure during scanning

**Correct Answer: C**

### Question 7

In the Orange Labs copy-move forgery detection example shown in the lecture, what would cause a "KO" (false negative) result?

- A) Too many SIFT features detected in the image
- B) Insufficient or inconsistent feature matches between copied regions
- C) High image resolution
- D) Presence of multiple objects in the scene

**Correct Answer: B**

### Question 8

The k-nearest neighbor search in SIFT-based image retrieval becomes computationally challenging primarily due to:

- A) The need to compare every query descriptor against all database descriptors
- B) SIFT descriptors being too small in size
- C) Inability to parallelize the search process
- D) Requirements for exact matches only

**Correct Answer: A**

### Question 9

In mobile visual search applications, SIFT features enable users to:

- A) Only search for text within images
- B) Query databases using visual content from their camera, robust to viewing conditions
- C) Automatically translate text in foreign languages
- D) Enhance photo quality before sharing

**Correct Answer: B**

### Question 10

The Page-Hinkley test mentioned in the content-based retrieval voting scheme is likely used to:

- A) Compress SIFT descriptors for storage efficiency
- B) Determine the optimal number of features to extract
- C) Make decisions about retrieval results based on accumulated evidence
- D) Convert SIFT features to binary representations

**Correct Answer: C**

---

## True/False Questions

### Question 1

**Statement:** In panorama creation, SIFT features are only useful for detecting overlapping regions, and the actual stitching process relies entirely on pixel-level blending algorithms.

**Answer: False**

**Explanation:** SIFT features play a crucial role beyond just detecting overlaps. They are essential for estimating the homography transformation between images, which is necessary for proper geometric alignment before blending. The lecture specifically mentions that SIFT helps "estimate homography between images" and "warp and blend the images," indicating SIFT's involvement in the geometric transformation process, not just overlap detection.

### Question 2

**Statement:** Copy-move forgery detection using SIFT works by identifying regions where the same features appear multiple times with consistent geometric transformations, regardless of minor modifications like scaling or rotation applied to the copied region.

**Answer: True**

**Explanation:** This statement correctly describes the principle behind SIFT-based copy-move detection. SIFT features are robust to affine transformations (including scaling and rotation), so even if a copied region is slightly modified, the algorithm can still detect consistent affine transformations among feature matches. The lecture mentions identifying "consistent affine transformations among matches" as the key mechanism.

### Question 3

**Statement:** In content-based image retrieval, using SIFT features with Bag-of-Words requires each query image to have exactly the same number of keypoints as the database images for accurate similarity comparison.

**Answer: False**

**Explanation:** The Bag-of-Words approach with SIFT is specifically designed to handle variable numbers of features. The voting mechanism accumulates evidence from individual descriptor matches, and the final similarity is based on the total votes received by each database image. The lecture shows that query images can have different numbers of descriptors (Q1, Q2, ..., Qn), and the system still works effectively by counting matches rather than requiring exact correspondence.

### Question 4

**Statement:** Video stabilization using SIFT features requires processing every single pixel in each frame to effectively remove camera jitter.

**Answer: False**

**Explanation:** Video stabilization with SIFT works by tracking sparse keypoints between frames, not every pixel. The process involves: 1) tracking keypoints between frames, 2) estimating a motion model from these sparse correspondences, and 3) smoothing the trajectory. This sparse approach is much more efficient than processing every pixel and is sufficient for estimating camera motion.

### Question 5

**Statement:** The main computational challenge in large-scale SIFT-based image retrieval systems is the k-nearest neighbor search, which requires comparing query descriptors against potentially millions of database descriptors.

**Answer: True**

**Explanation:** The lecture explicitly identifies "Efficiency is the main challenge" for nearest neighbor search and shows the computational burden of comparing query descriptors against large databases. With high-dimensional SIFT descriptors (typically 128 dimensions) and potentially millions of database descriptors, the search becomes computationally intensive, requiring specialized indexing structures and approximate search methods for practical applications.

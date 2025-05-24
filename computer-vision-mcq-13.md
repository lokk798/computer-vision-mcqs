# Part 13

# Computer Vision SIFT Quiz - Tricky Questions

## Multiple Choice Questions (MCQs)

### Question 1

In the SIFT blob detection process, when checking for local maxima, how many neighbors does each candidate point need to be compared against?

- A) 8 neighbors (same scale only)
- B) 18 neighbors (current scale + one adjacent scale)
- C) 26 neighbors (current scale + two adjacent scales)
- D) 24 neighbors (excluding the center point)

**Correct Answer: C**

### Question 2

The Difference of Gaussians (DoG) approximation in SIFT is mathematically equivalent to which operation?

- A) Laplacian of Gaussian (LoG)
- B) Gradient magnitude
- C) Second derivative operator
- D) Sobel edge detector

**Correct Answer: A**

### Question 3

In the SIFT descriptor computation, the 16×16 window around each keypoint is divided into cells. What is the dimensionality of the final descriptor vector?

- A) 64 dimensions (16 cells × 4 bins)
- B) 128 dimensions (16 cells × 8 bins)
- C) 256 dimensions (16 cells × 16 bins)
- D) 32 dimensions (8 cells × 4 bins)

**Correct Answer: B**

### Question 4

Which of the following best describes the relationship between octaves and Gaussian scale (σ) in SIFT?

- A) Octaves and σ are the same thing, just different terminology
- B) Octaves handle spatial resolution reduction, while σ controls smoothing within each octave
- C) σ values reset to zero at the start of each new octave
- D) Octaves are used only for descriptor computation, not for detection

**Correct Answer: B**

### Question 5

In SIFT descriptor normalization, why are values clamped to 0.2 before renormalization?

- A) To reduce computational complexity
- B) To prevent large gradients from dominating the descriptor
- C) To ensure rotation invariance
- D) To maintain scale invariance

**Correct Answer: B**

### Question 6

When computing the principal orientation for a SIFT keypoint, what information is primarily used?

- A) The DoG response magnitude
- B) The local image intensity values
- C) The histogram of gradient directions
- D) The scale space location

**Correct Answer: C**

### Question 7

In the context of SIFT, what happens to the image size as you move from one octave to the next?

- A) It remains the same
- B) It doubles in both width and height
- C) It is halved in both width and height
- D) Only the width is halved

**Correct Answer: C**

### Question 8

For SIFT descriptor matching, which distance metric was mentioned in the lecture for comparing two 128-dimensional descriptors?

- A) Manhattan distance only
- B) Cosine similarity only
- C) Both Euclidean distance and histogram intersection
- D) Hamming distance only

**Correct Answer: C**

### Question 9

What is the primary advantage of applying Gaussian weighting when computing orientation histograms in SIFT descriptors?

- A) It reduces computational cost
- B) It gives more importance to gradients near the keypoint center
- C) It eliminates the need for normalization
- D) It automatically handles scale changes

**Correct Answer: B**

### Question 10

In the Local Binary Pattern (LBP) descriptor mentioned in the lecture, how is the binary pattern generated for a 3×3 neighborhood?

- A) Compare each neighbor to a fixed threshold value
- B) Compare each neighbor to the center pixel value
- C) Compare adjacent neighbors to each other
- D) Use gradient magnitude comparisons

**Correct Answer: B**

## True/False Questions

### Question 1

**Statement:** In SIFT, the same keypoint detected at different octaves will have identical coordinate values (x,y) in the image space.

**Answer: FALSE**

**Explanation:** This is false because different octaves represent different image resolutions. When an image is downsampled for a new octave (halved in width and height), the coordinate system changes. A keypoint that appears at coordinates (100, 200) in the original image might appear at coordinates (50, 100) in the next octave due to the downsampling. The keypoint represents the same physical location in the scene, but its pixel coordinates differ across octaves.

### Question 2

**Statement:** The SIFT descriptor's rotation invariance is achieved solely through the normalization process (L2 norm) applied to the 128-dimensional feature vector.

**Answer: FALSE**

**Explanation:** This is false because rotation invariance in SIFT is primarily achieved by rotating the 16×16 descriptor window according to the keypoint's principal orientation before computing the descriptor. The gradient orientations are also computed relative to this principal orientation. The L2 normalization is performed for illumination invariance, not rotation invariance. Without the orientation alignment step, the descriptor would not be rotation invariant regardless of normalization.

### Question 3

**Statement:** In SIFT blob detection, applying a threshold after extracting local maxima is necessary because all local maxima in the DoG pyramid represent equally strong interest points.

**Answer: FALSE**

**Explanation:** This is false because not all local maxima represent equally strong or reliable interest points. Some local maxima may have very low contrast or may be located along edges rather than at distinctive corners or blobs. The threshold is applied to filter out weak responses and ensure that only sufficiently strong and distinctive keypoints are retained. Without thresholding, many unstable or unreliable keypoints would be included, reducing the overall quality of feature matching.

### Question 4

**Statement:** The histogram intersection distance for SIFT descriptor matching produces larger values for better matches, unlike the Euclidean distance which produces smaller values for better matches.

**Answer: TRUE**

**Explanation:** This is true. In histogram intersection, the distance is computed as the sum of minimum values between corresponding bins of two histograms. When two descriptors are very similar, many corresponding bins will have similar values, leading to a larger intersection sum, indicating a better match. In contrast, Euclidean distance measures the geometric distance between two points in 128-dimensional space, where smaller distances indicate better matches (more similar descriptors).

### Question 5

**Statement:** The reason SIFT uses a 16×16 window divided into 4×4 cells rather than computing a single histogram for the entire window is purely to reduce computational complexity.

**Answer: FALSE**

**Explanation:** This is false because the primary reason for dividing the window into 4×4 cells is to capture spatial information and provide spatial granularity to the descriptor. A single histogram for the entire 16×16 window would lose spatial relationships between different parts of the local neighborhood. The 4×4 cell division allows the descriptor to encode not just what gradient orientations are present, but also where they are located within the local neighborhood, making the descriptor much more distinctive and robust for matching. This actually increases computational complexity compared to a single histogram, but provides much better discriminative power.

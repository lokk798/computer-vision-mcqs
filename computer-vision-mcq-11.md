# Part 11

# Computer Vision Corner Detection Quiz

## Multiple Choice Questions (MCQ)

### Question 1

In the Harris corner detector, what does the structure tensor M represent?

- A weighted sum of image intensities in a local window
- A covariance-like matrix of gradient vectors in a local neighborhood
- The direct computation of eigenvalues at each pixel
- The convolution of the image with a Gaussian kernel

**Correct Answer: B**

### Question 2

Which statement about eigenvalues λ₁ and λ₂ in corner detection is most accurate?

- λ₁ is always larger than λ₂ by definition
- Both eigenvalues represent intensity changes in the same direction
- λ₁ represents maximum inertia direction, λ₂ represents minimum inertia direction
- The eigenvalues are independent of the local gradient distribution

**Correct Answer: C**

### Question 3

In the Harris corner response function R = det(M) - k·trace(M)², what is the typical range for the parameter k?

- [0.01, 0.02]
- [0.04, 0.06]
- [0.1, 0.2]
- [0.5, 1.0]

**Correct Answer: B**

### Question 4

What is the primary reason edge detectors perform poorly at corners?

- Corners have lower contrast than edges
- At corners, the gradient direction is ill-defined due to multiple edge directions meeting
- Corners occur less frequently than edges in natural images
- Edge detectors are designed only for horizontal and vertical features

**Correct Answer: B**

### Question 5

In the context of corner detection invariance, which transformation poses the greatest challenge for the basic Harris detector?

- Translation of the image
- Rotation of the image
- Large-scale changes in object size
- Small illumination variations

**Correct Answer: C**

### Question 6

What distinguishes the Shi-Tomasi corner detector from the Harris detector?

- Shi-Tomasi uses a different structure tensor formulation
- Shi-Tomasi directly uses min(λ₁, λ₂) > threshold instead of the Harris response function
- Shi-Tomasi computes gradients in three directions instead of two
- Shi-Tomasi applies non-maximal suppression differently

**Correct Answer: B**

### Question 7

In the gradient distribution visualization shown in the lecture, what characterizes a flat region?

- High variance in both x and y gradient directions
- High variance in x direction, low variance in y direction
- Low variance in both x and y gradient directions
- High variance in one diagonal direction only

**Correct Answer: C**

### Question 8

What is the mathematical relationship between det(M) and trace(M) in terms of eigenvalues?

- det(M) = λ₁ + λ₂, trace(M) = λ₁ × λ₂
- det(M) = λ₁ × λ₂, trace(M) = λ₁ + λ₂
- det(M) = λ₁ - λ₂, trace(M) = λ₁ + λ₂
- det(M) = λ₁ + λ₂, trace(M) = λ₁ - λ₂

**Correct Answer: B**

### Question 9

In the Non-Maximal Suppression technique for corner detection, what is the primary purpose?

- To increase the number of detected corners
- To convert corner detection into an edge detection problem
- To eliminate weak corners and retain only local maxima
- To smooth the corner response function

**Correct Answer: C**

### Question 10

What makes the Förstner detector unique compared to Harris and Shi-Tomasi detectors?

- It only uses one eigenvalue for detection
- It provides both corner strength and precision/accuracy measures
- It works exclusively with binary images
- It requires manual parameter tuning for each image

**Correct Answer: B**

---

## True/False Questions

### Question 1

**Statement:** The Harris corner detector is completely invariant to all types of scaling transformations in images.

**Answer: False**

**Explanation:** The Harris detector is only partially invariant to scaling and has limited scale invariance. For small scaling changes it performs well, but it requires multi-scale analysis to handle large variations in size. The basic Harris detector does not automatically adapt to different scales, which is why scale-invariant extensions like SIFT were developed.

### Question 2

**Statement:** In corner detection, when both eigenvalues λ₁ and λ₂ of the structure tensor are small, this indicates the presence of a strong corner.

**Answer: False**

**Explanation:** When both eigenvalues are small, this indicates a flat region with little intensity variation in any direction. A corner is characterized by both eigenvalues being large, indicating significant intensity changes in multiple orthogonal directions. The eigenvalue interpretation is: both small = flat region, one large = edge, both large = corner.

### Question 3

**Statement:** The weighting function w(x,y) in the Harris structure tensor is typically a Gaussian function that gives equal importance to all pixels in the analysis window.

**Answer: False**

**Explanation:** The Gaussian weighting function specifically gives MORE importance to pixels near the center of the window, not equal importance to all pixels. This weighting scheme helps focus the analysis on the immediate neighborhood of the pixel being evaluated and reduces the influence of distant pixels, making the corner detection more localized and robust.

### Question 4

**Statement:** The corner response score R in the Harris detector can be directly computed without knowing the actual eigenvalues λ₁ and λ₂ of the structure tensor M.

**Answer: True**

**Explanation:** This is correct. The Harris response function R = det(M) - k·trace(M)² uses det(M) = λ₁λ₂ and trace(M) = λ₁ + λ₂, but these can be computed directly from the structure tensor elements without explicitly calculating the eigenvalues. This is computationally more efficient than performing eigenvalue decomposition at every pixel.

### Question 5

**Statement:** According to the lecture, corner detection is essentially a peak detection problem after computing the corner response function.

**Answer: True**

**Explanation:** This is correct. Once the Harris corner response function R is computed for all pixels, corner detection becomes a matter of finding peaks (local maxima) in this response. Corners appear as clusters of high-response points, and techniques like thresholding and non-maximal suppression are used to identify and isolate these peaks, converting the corner detection problem into a peak detection problem.

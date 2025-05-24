# Part 7

## Multiple Choice Questions (MCQs)

### Question 1
When applying gradient-based edge detection, what happens if you use a very high threshold value?

- A) You get more noise in the edge map
- B) You get thicker edge lines
- C) Important edges may be missed
- D) The computational cost increases significantly

**Correct Answer: C**

### Question 2
In the context of edge models, which statement best describes the relationship between ramp edges and image blurring?

- A) The steeper the ramp, the more blurred the edge
- B) The slope of the ramp is directly proportional to the degree of blurring
- C) The slope of the ramp is inversely proportional to the degree of blurring
- D) Ramp edges are unaffected by blurring

**Correct Answer: C**

### Question 3
Which of the following best explains why we apply ∇(n_σ * f) = ∇n_σ * f in derivative of Gaussian filtering?

- A) Because Gaussian filtering is non-linear
- B) Because both gradient and Gaussian smoothing are linear operations
- C) Because it reduces computational complexity only
- D) Because it eliminates the need for thresholding

**Correct Answer: B**

### Question 4
In hysteresis-based thresholding with thresholds T₀ < T₁, a pixel with gradient magnitude between T₀ and T₁ will be classified as:

- A) Definitely an edge
- B) Definitely not an edge
- C) An edge only if a neighboring pixel is definitely an edge
- D) An edge only if all neighboring pixels are definitely edges

**Correct Answer: C**

### Question 5
What is the primary limitation of using Laplacian for edge detection compared to gradient-based methods?

- A) Laplacian is more sensitive to noise
- B) Laplacian requires more computational resources
- C) Laplacian does not provide the direction of edges
- D) Laplacian cannot detect step edges

**Correct Answer: C**

### Question 6
In the Sobel operator implementation shown in the lecture, why are there two separate convolution kernels?

- A) One for horizontal edges and one for vertical edges
- B) One for detecting step edges and one for ramp edges
- C) One for ∂I/∂x and one for ∂I/∂y partial derivatives
- D) One for noise reduction and one for edge enhancement

**Correct Answer: C**

### Question 7
When detecting zero-crossings in Laplacian edge detection, what additional condition is typically required besides sign change?

- A) The gradient magnitude must exceed a threshold
- B) The absolute difference must be large enough to avoid noise-induced sign flips
- C) The pixel must be a local maximum
- D) All 8-connected neighbors must have the same sign

**Correct Answer: B**

### Question 8
According to the lecture's edge models, roof edges are most commonly found in:

- A) Boundaries between objects of different colors
- B) Areas with depth discontinuities
- C) Thin structures like wires or roads in aerial images
- D) Shadow boundaries in out-of-focus regions

**Correct Answer: C**

### Question 9
What does the "inverted sombrero" or "Mexican hat" shape represent in the context of edge detection?

- A) The 1D profile of a Sobel operator
- B) The 2D profile of Laplacian of Gaussian (∇²G)
- C) The gradient magnitude distribution
- D) The hysteresis thresholding function

**Correct Answer: B**

### Question 10
Why is image smoothing considered a "mandatory step" prior to using derivatives for edge detection?

- A) To enhance edge contrast
- B) To reduce computational complexity
- C) To mitigate noise that can cause false edge interpretation
- D) To convert the image to grayscale

**Correct Answer: C**

---

## True/False Questions

### Question 1
**Statement**: In gradient-based edge detection, the edge orientation is parallel to the gradient direction.

**Answer**: False

**Explanation**: The edge orientation is orthogonal (perpendicular) to the gradient direction, not parallel. The gradient points in the direction of maximum intensity change, while the edge runs perpendicular to this direction. This is explicitly stated in the lecture: "Edge orientation (orthogonal to the gradient direction)."

### Question 2
**Statement**: The Laplacian operator ∇²I = ∂²I/∂x² + ∂²I/∂y² requires two separate convolutions to compute, similar to gradient-based methods.

**Answer**: False

**Explanation**: The Laplacian is a linear operation that requires only one convolution, unlike gradient-based methods which are non-linear operations requiring two convolutions (one for ∂I/∂x and one for ∂I/∂y). This is one of the computational advantages of Laplacian-based edge detection mentioned in the lecture comparison.

### Question 3
**Statement**: In the discrete Laplacian kernels shown in the lecture, all three versions (standard 3×3, weighted, and 8-connected) will produce identical zero-crossing locations for the same image.

**Answer**: False

**Explanation**: Different Laplacian kernel implementations have different characteristics regarding localization accuracy and noise sensitivity. The standard kernel, weighted kernel, and 8-connected kernel will generally produce similar but not identical results, with variations in sensitivity and localization precision.

### Question 4
**Statement**: According to the performance requirements mentioned in the lecture, a good edge detector should have high detection rate, good localization, and high sensitivity to noise.

**Answer**: False

**Explanation**: The lecture explicitly states that a good edge detector should have "low sensitivity to noise," not high sensitivity. High sensitivity to noise would be detrimental as it would cause the detector to respond to noise as if it were genuine edges, reducing the overall performance.

### Question 5
**Statement**: The Henry Moore sculpture example demonstrates that biological vision systems primarily rely on processing all pixel intensities rather than focusing on edges and local features.

**Answer**: False

**Explanation**: The Henry Moore sculpture example actually demonstrates the opposite - that focusing on edges (as shown in the artist's sketch) can convey substantial information about 3D structure and lighting effects. The lecture uses this to support the biological plausibility argument that "initial stages of mammalian vision systems involve detection of edges and local features," not processing all pixel intensities.
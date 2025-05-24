# Part 8

# Canny Edge Detector - Quiz Questions

## Multiple Choice Questions (MCQs)

### Question 1

What is the primary reason why Canny's edge detector uses both gradient magnitude and Laplacian operations?

- A) To reduce computational complexity by combining two operations
- B) To satisfy the three optimality criteria: low error rate, good localization, and single response
- C) To make the algorithm work faster on large images
- D) To eliminate the need for Gaussian smoothing

**Correct Answer: B**

### Question 2

In the context of Canny's mathematical formulation, what does maximizing the compromise criterion Λ(F) × σ(F) actually achieve?

- A) It minimizes both localization error and detection error simultaneously
- B) It finds the optimal balance between good localization (Λ) and good detection (σ)
- C) It ensures that the filter F produces the fastest computation time
- D) It guarantees that only step edges are detected

**Correct Answer: B**

### Question 3

During non-maxima suppression in the Canny algorithm, a pixel's gradient magnitude is set to zero if:

- A) It's smaller than both neighbors along the gradient direction
- B) It's smaller than at least one neighbor along the gradient direction
- C) It's smaller than all eight neighbors in the 3×3 window
- D) It's below the lower threshold T₀

**Correct Answer: B**

### Question 4

In hysteresis thresholding, a pixel with gradient magnitude between T₀ and T₁ becomes an edge pixel when:

- A) It's connected to any pixel above T₁ in the entire image
- B) It has at least one neighboring pixel that is definitely an edge (≥ T₁)
- C) Its gradient direction is consistent with nearby pixels
- D) It survives the non-maxima suppression step

**Correct Answer: B**

### Question 5

Why does the Canny detector compute the 1D Laplacian along the gradient direction rather than the standard 2D Laplacian?

- A) To reduce computational cost from O(n²) to O(n)
- B) To ensure that only the strongest edges are detected
- C) To find precise edge locations by detecting zero-crossings perpendicular to the edge
- D) To eliminate the need for non-maxima suppression

**Correct Answer: C**

### Question 6

When comparing the Lena image results with σ = 1, σ = 2, and σ = 4, what trade-off is being demonstrated?

- A) Speed vs accuracy - larger σ means faster computation
- B) Noise reduction vs edge preservation - larger σ reduces noise but may lose fine details
- C) Memory usage vs image quality - larger σ requires less memory
- D) Threshold sensitivity vs robustness - larger σ makes thresholding unnecessary

**Correct Answer: B**

### Question 7

In Pratt's Figure of Merit (FOM) formula, what does the parameter α (typically 1/9) control?

- A) The maximum allowed distance between detected and ground truth edges
- B) The penalty applied to detected edges that are far from ground truth edges
- C) The weight given to precision versus recall in the final score
- D) The normalization factor for different image sizes

**Correct Answer: B**

### Question 8

The optical illusions shown (Hering and Café wall) are relevant to edge detection because they demonstrate:

- A) How human vision can be tricked by algorithmic edge detection
- B) That edge detection algorithms are superior to human perception
- C) The difference between perceptual edges and intensity-based edges
- D) Why Gaussian smoothing is essential in edge detection

**Correct Answer: C**

### Question 9

When evaluating edge detectors using the BSDS500 dataset, why is "small tolerance in edge location" mentioned as a best practice?

- A) Because human annotators are inherently imprecise
- B) Because detected edges may be slightly shifted due to discretization and algorithm approximations
- C) Because the dataset contains measurement errors
- D) Because different edge detectors use different coordinate systems

**Correct Answer: B**

### Question 10

In the step-by-step Canny algorithm, why is the gradient direction (n̂) calculated as a unit vector?

- A) To normalize the gradient magnitude across different scales
- B) To ensure consistent direction representation regardless of gradient strength
- C) To simplify the computation of the 1D Laplacian along that direction
- D) To make the non-maxima suppression step more efficient

**Correct Answer: B**

---

## True/False Questions

### Question 1

**Statement:** In the Canny edge detector, the non-maxima suppression step and computing the 1D Laplacian along the gradient direction serve the same purpose and are interchangeable approaches.

**Answer: True**

**Explanation:** According to the lecture, step 3 can be presented as either "non-maxima suppression" or "a 1D Laplacian operator." Both approaches achieve the same goal of keeping only local maxima in the gradient direction to thin the edges and ensure single-pixel-wide edge responses.

### Question 2

**Statement:** The boundary displacement error (BDE) metric becomes less important when evaluating edge detectors on high-resolution images compared to low-resolution images.

**Answer: False**

**Explanation:** The opposite is true. The lecture specifically mentions that "Edge Localization Error" is "especially important in high-resolution images or critical applications." In high-resolution images, even small displacement errors become more significant and can affect the practical utility of the edge detection results.

### Question 3

**Statement:** A pixel with gradient magnitude exactly equal to T₁ in hysteresis thresholding is automatically classified as a definite edge pixel without needing to check its neighbors.

**Answer: True**

**Explanation:** According to the hysteresis thresholding rules presented: "∇I(x,y) ≥ T₁: Definitely an edge." Since the pixel's gradient magnitude equals T₁, it satisfies the ≥ T₁ condition and is definitively classified as an edge pixel.

### Question 4

**Statement:** The reason Canny's algorithm is considered optimal is primarily because it runs faster than other edge detection methods while maintaining similar accuracy.

**Answer: False**

**Explanation:** Canny's optimality is not about computational speed but about satisfying three specific criteria mathematically: (1) low error rate, (2) good localization, and (3) single edge point response. The lecture emphasizes that Canny expressed these criteria mathematically and found optimal solutions, not that it was designed for speed.

### Question 5

**Statement:** In quantitative evaluation of edge detectors, having both high precision and high recall simultaneously always guarantees a Pratt's Figure of Merit (FOM) score close to 1.

**Answer: False**

**Explanation:** While high precision and recall are important, FOM specifically measures the quality of edge localization by considering the distance (dᵢ) between detected edges and ground truth edges. Even with perfect precision and recall, if the detected edges are consistently displaced from their true positions, the FOM score will be penalized by the distance term in the formula, preventing it from reaching 1.

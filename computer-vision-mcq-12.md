# Part 12

# SIFT Computer Vision Quiz - Tricky Questions

## Multiple Choice Questions (MCQs)

### 1. According to the lecture, what is the primary mathematical operation used in the SIFT detector for blob detection in 2D images?

- A) Gradient magnitude computation
- B) Normalized Laplacian of Gaussian (NLoG)
- C) Second derivative along edges
- D) Difference of Gaussians (DoG)

**Correct Answer: B) Normalized Laplacian of Gaussian (NLoG)**

### 2. In the 1D blob detection example shown in the lecture, each blob is detected as a minimum/maximum of which specific mathematical expression?

- A) σ · ∂²f/∂x²
- B) σ² · ∂²f/∂x²
- C) σ² · ∂²n_σ/∂x² \* f(x)
- D) ∂²n_σ/∂x² \* f(x)

**Correct Answer: C) σ² · ∂²n_σ/∂x² \* f(x)**

### 3. Based on the lecture's visual demonstrations, why are lines/edges NOT considered good interest points for SIFT?

- A) They lack scale invariance
- B) They don't provide rich image content within the window
- C) They have ambiguous position along the edge direction
- D) They are sensitive to illumination changes

**Correct Answer: C) They have ambiguous position along the edge direction**

### 4. The lecture mentions that blobs have a "characteristic scale." What does this characteristic scale represent?

- A) The σ value where the blob appears most circular
- B) The σ value where the normalized second derivative achieves its extremum
- C) The σ value where the blob has maximum contrast
- D) The σ value where the blob covers exactly 9 pixels

**Correct Answer: B) The σ value where the normalized second derivative achieves its extremum**

### 5. In the scale-space representation shown in the lecture, what happens when there is "no significant maximum" across scales?

- A) The detector creates a synthetic blob
- B) The algorithm interpolates between adjacent scales
- C) No blob is detected at that location
- D) The system defaults to the largest scale value

**Correct Answer: C) No blob is detected at that location**

### 6. According to the lecture, which property is NOT mentioned as a desired characteristic of interest points?

- A) Rich image content within the window
- B) Well-defined position in the image
- C) Invariance to perspective transformations
- D) Insensitivity to lighting changes

**Correct Answer: C) Invariance to perspective transformations**

### 7. The lecture shows that the characteristic scale is proportional to blob size. If blob A has characteristic scale σ_A = 2 and blob B has characteristic scale σ_B = 6, what can we conclude?

- A) Blob B is exactly 3 times larger than blob A
- B) Blob B is approximately 3 times larger than blob A
- C) Blob A and B have the same size but different orientations
- D) The relationship cannot be determined without additional information

**Correct Answer: B) Blob B is approximately 3 times larger than blob A**

### 8. In the SIFT algorithm's blob detection phase, the final step involves finding (x*, y*, σ\*). What does this notation represent?

- A) The coordinates and scale that minimize the NLoG response
- B) The coordinates and scale that maximize the absolute NLoG response
- C) The coordinates and scale that maximize the σ²∇²n_σ \* I(x,y) expression
- D) The centroid and average scale of all detected blobs

**Correct Answer: C) The coordinates and scale that maximize the σ²∇²n_σ \* I(x,y) expression**

### 9. Based on the lecture's discussion of SIFT advantages, which statement best explains why "locality" makes SIFT robust to occlusion?

- A) Local features can be matched even when parts of the object are hidden
- B) Local features are computed faster than global features
- C) Local features require less memory storage
- D) Local features are more distinctive than global features

**Correct Answer: A) Local features can be matched even when parts of the object are hidden**

### 10. The lecture mentions that SIFT "changed the way we approach many computer vision problems." Which combination of invariances makes SIFT particularly revolutionary?

- A) Translation and rotation only
- B) Scale and illumination only
- C) Scaling, rotation, and illumination while maintaining good localization
- D) All possible geometric transformations

**Correct Answer: C) Scaling, rotation, and illumination while maintaining good localization**

---

## True/False Questions

### 1. True/False: According to the lecture, blobs are always circular regions in images.

**Answer: False**

**Explanation:** The lecture explicitly states that blobs are "not necessarily circular, though often approximated as such for analysis." Blobs refer to regions that are visually distinct from their surroundings in terms of brightness, color, or texture, but they don't have to be perfectly circular in shape.

### 2. True/False: In the 1D blob detection example, larger σ values are used to detect smaller blobs.

**Answer: False**

**Explanation:** This is counterintuitive but incorrect. The lecture shows that the characteristic scale σ is proportional to the size of the blob. Larger σ values correspond to larger blobs, while smaller σ values detect smaller blobs. The characteristic scale represents the "natural" scale at which a blob should be detected.

### 3. True/False: The SIFT detector consists of three main components: keypoint localization, descriptor computation, and descriptor matching.

**Answer: False**

**Explanation:** The lecture states that SIFT consists of "two parts": (1) A detector of interest area (keypoint localization) and (2) A local signature computation method (descriptor). While descriptor matching is mentioned as an application that uses SIFT descriptors, it's not considered one of the core components of the SIFT algorithm itself.

### 4. True/False: According to the scale-space illustration in the lecture, the same physical blob in an image will produce maximum responses at the same σ value regardless of the blob's actual size.

**Answer: False**

**Explanation:** This is a tricky question about the fundamental principle of scale-space analysis. Different sized blobs will produce maximum responses at different σ values. The whole point of the characteristic scale concept is that each blob has its own optimal σ value that corresponds to its size - larger blobs are detected at larger σ values.

### 5. True/False: The normalization factor σ² in the normalized Laplacian of Gaussian is essential for achieving scale invariance in blob detection.

**Answer: True**

**Explanation:** The σ² normalization factor is crucial for scale invariance. Without this normalization, the response of the Laplacian of Gaussian would decrease as σ increases, making it impossible to compare responses across scales fairly. The σ² factor ensures that blobs of different sizes can be detected and compared on equal footing across the scale space.

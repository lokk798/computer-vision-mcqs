# Part 9

# Computer Vision Quiz: Line/Curve Detection & Hough Transform

## Multiple Choice Questions (MCQs)

### 1. When fitting a line using least squares method with the equation y = mx + c, what is the main limitation that necessitates switching to polar representation?

- A) The method cannot handle curved lines
- B) Vertical lines cause the slope parameter m to approach infinity
- C) The method is computationally too expensive
- D) It cannot handle multiple lines in the same image

**Answer: B**

### 2. In the Hough transform for line detection, each point in the image space corresponds to what in the parameter space?

- A) A single point representing the line parameters
- B) A sinusoidal curve in the (ρ, θ) parameter space
- C) A straight line in the (m, c) parameter space
- D) A circle in the parameter space

**Answer: B**

### 3. When using PCA for fitting lines by minimizing perpendicular distances, the normal direction of the fitted line corresponds to:

- A) The eigenvector with the largest eigenvalue
- B) The eigenvector with the smallest eigenvalue
- C) The mean of all eigenvectors
- D) The sum of all eigenvectors

**Answer: B**

### 4. In the matrix formulation Xa = y for polynomial curve fitting, if we have 100 data points and want to fit a 3rd degree polynomial, what are the dimensions of matrix X?

- A) 3 × 100
- B) 100 × 3
- C) 4 × 100
- D) 100 × 4

**Answer: D**

### 5. For circle detection using Hough transform with unknown radius, the parameter space becomes three-dimensional (a, b, r). What geometric shape does each image point create in this 3D parameter space?

- A) A plane
- B) A cone
- C) A sphere
- D) A cylinder

**Answer: B**

### 6. The pseudo-inverse X⁺ = (X^T X)^(-1) X^T is used in curve fitting when:

- A) The system is under-determined
- B) The system is exactly determined
- C) The system is over-determined
- D) The matrix X is square

**Answer: C**

### 7. In the Hough transform accumulator array, what does a high-value peak specifically represent?

- A) The presence of noise in the image
- B) A set of collinear edge points voting for the same line parameters
- C) The strongest edge in the image
- D) The center of the image

**Answer: B**

### 8. When optimizing the Hough transform using gradient direction information, the main advantage is:

- A) It eliminates the need for edge detection
- B) It reduces the range of θ values that need to be tested for each point
- C) It automatically finds the optimal quantization
- D) It removes the need for an accumulator array

**Answer: B**

### 9. The three sub-problems in curve fitting are parameter estimation, token-curve association, and counting. Which is the most challenging computationally?

- A) Parameter estimation, because it requires matrix inversion
- B) Token-curve association, because it's a combinatorial problem
- C) Counting, because it requires prior knowledge
- D) All three are equally challenging

**Answer: C**

### 10. In circle detection with known radius r, if an image point (xi, yi) votes in the parameter space, the locus of possible circle centers forms:

- A) A straight line
- B) A circle of radius r centered at (xi, yi)
- C) A point at (xi, yi)
- D) An ellipse

**Answer: B**

---

## True/False Questions

### 1. In the Hough transform, the quantization resolution directly affects both memory requirements and detection accuracy - finer quantization always leads to better results.

**Answer: False**

**Explanation:** While finer quantization increases memory requirements, it doesn't always lead to better results. Fine quantization can cause vote dispersion where votes for the same geometric feature get spread across multiple nearby bins, potentially causing the feature to be missed. Conversely, coarse quantization might merge different features together. The optimal resolution is a trade-off between precision and robustness.

### 2. When fitting a polynomial curve y = ax³ + bx² + cx + d to edge points, the resulting system of equations can always be solved uniquely if we have exactly 4 data points.

**Answer: False**

**Explanation:** Having exactly 4 points for 4 unknowns creates a square system, but it can only be solved uniquely if the points are not collinear and the coefficient matrix is invertible (non-singular). If the points are positioned such that the resulting matrix is singular (determinant = 0), the system may have no solution or infinitely many solutions. Additionally, having exactly the minimum number of points provides no robustness against noise.

### 3. In the polar representation of the Hough transform (ρ = x cos θ + y sin θ), the parameter ρ can take negative values and this is essential for detecting all possible line orientations.

**Answer: True**

**Explanation:** The parameter ρ represents the signed perpendicular distance from the origin to the line. It can indeed be negative, and this is crucial for representing lines on both sides of the origin. If ρ were restricted to positive values only, we could only detect lines on one side of the origin, significantly limiting the transform's capability. The negative values allow the algorithm to detect lines in all orientations and positions relative to the coordinate system origin.

### 4. The least squares method for line fitting by minimizing vertical distances (y = mx + c) and the PCA method for minimizing perpendicular distances will always produce identical results regardless of the data distribution.

**Answer: False**

**Explanation:** These methods minimize different error metrics and generally produce different results. The least squares method minimizes vertical distances (errors in y-direction only), while PCA minimizes perpendicular distances to the line. They only produce identical results in very specific cases, such as when the data points are perfectly aligned or when the line is horizontal. For most real-world data distributions, especially when points don't follow a clear horizontal/vertical pattern, the results will differ significantly.

### 5. In circle detection using Hough transform, if we know the radius r beforehand, the computational complexity is always lower than line detection because we're working with a 2D parameter space (a, b) instead of the line's 2D space (ρ, θ).

**Answer: False**

**Explanation:** While both use 2D parameter spaces, circle detection is generally more computationally expensive than line detection. In line detection, each image point contributes to a 1D curve (sinusoid) in parameter space. In circle detection with known radius, each image point contributes to a full circle in the (a, b) parameter space, requiring computation and voting for many more parameter combinations. The circular locus in parameter space involves more trigonometric calculations and accumulator updates compared to the sinusoidal curve of line detection.

---



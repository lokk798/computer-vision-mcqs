# Computer Vision Part 5: Correlation and Convolution MCQ Test

## Multiple Choice Questions (20)

### 1. What is the fundamental difference between correlation and convolution?

- A) Correlation uses addition while convolution uses multiplication
- B) Correlation uses a sliding window approach while convolution uses a fixed window
- C) In convolution, the filter mask is first rotated by 180° before sliding
- D) Correlation is used for images while convolution is used for signals
  **Answer: C**

### 2. When correlating a filter w with a function that contains all 0s and a single 1, what is the result?

- A) A function with all 0s
- B) A copy of the filter w
- C) A copy of w, rotated by 180°
- D) A function with all 1s
  **Answer: C**

### 3. In template matching, minimizing E[i,j] is equivalent to maximizing:

- A) The squared sum of the template
- B) The squared sum of the image region
- C) The correlation between the template and image region
- D) The difference between template and image
  **Answer: C**

### 4. What is the main limitation of using simple correlation for pattern matching?

- A) It's computationally expensive
- B) It can't handle patterns larger than the filter
- C) The response might be large just because the image region is bright
- D) It only works on grayscale images
  **Answer: C**

### 5. For a 2D image and a filter of size MxN, what is the minimum padding required?

- A) M rows at top, M rows at bottom, N columns at left, N columns at right
- B) M-1 rows at top, M-1 rows at bottom, N-1 columns at left, N-1 columns at right
- C) M/2 rows at top, M/2 rows at bottom, N/2 columns at left, N/2 columns at right
- D) No padding is required
  **Answer: B**

### 6. What does normalized correlation accomplish that simple correlation does not?

- A) It makes the correlation faster to compute
- B) It makes the correlation insensitive to brightness
- C) It makes the correlation insensitive to rotation
- D) It makes the correlation insensitive to scaling
  **Answer: B**

### 7. In the normalized correlation formula, what do the terms in the denominator represent?

- A) The size of the template and image
- B) The average values of the template and image
- C) The energy (sum of squares) of the template and image region
- D) The maximum values of the template and image
  **Answer: C**

### 8. When a filter responds most strongly to an image pattern, what can be said about the relationship between the filter and image pattern?

- A) They are perpendicular to each other when viewed as vectors
- B) They are parallel to each other when viewed as vectors
- C) Their dot product equals zero
- D) Their cross-correlation equals zero
  **Answer: B**

### 9. If we convolve a function with a unit impulse, what is the result?

- A) A unit impulse at the same location
- B) A copy of the function
- C) A copy of the mask at the location of the impulse
- D) All zeros except at the impulse location
  **Answer: C**

### 10. Given a 1D signal f(x) = [0,0,0,1,0,0,0,0] and a mask w(x) = [1,2,3,2,8], what is the value of the first element of the correlation output?

- A) 0
- B) N/A (not enough information)
- C) 1
- D) 8
  **Answer: A**

### 11. In template matching using correlation, the process can be interpreted as:

- A) Finding the location where the template has minimum overlap with the image
- B) Finding the location where the difference between template and image is minimized
- C) Finding the location where the template and image have maximum similarity
- D) Finding the location where the gradients of the template and image match
  **Answer: C**

### 12. The correlation operation can be defined as a:

- A) Matrix multiplication
- B) Dot product between image regions and the filter
- C) Cross product between image regions and the filter
- D) Element-wise division between image and filter
  **Answer: B**

### 13. What mathematical operation is performed at each location when computing correlation?

- A) Addition of the filter values
- B) Multiplication of the filter values
- C) Sum of products between filter values and corresponding image values
- D) Average of filter values and image values
  **Answer: C**

### 14. Which of the following is NOT a property of convolution?

- A) Convolving with a unit impulse yields the original signal
- B) Convolution is commutative (a⨂b = b⨂a)
- C) Convolution is associative ((a⨂b)⨂c = a⨂(b⨂c))
- D) Convolution always increases the size of the output signal
  **Answer: D**

### 15. For a filter of size 3×3, how many multiplications are required to compute one output pixel in correlation?

- A) 3
- B) 6
- C) 9
- D) 12
  **Answer: C**

### 16. What happens to the dimensions of an image after correlation with a filter without any padding?

- A) The output dimensions increase
- B) The output dimensions decrease
- C) The output dimensions remain the same
- D) The output dimensions become equal to the filter dimensions
  **Answer: B**

### 17. In the equation for normalized correlation, what is the purpose of taking the square root of the product of energy terms?

- A) To ensure the result is in the range [-1, 1]
- B) To make the computation faster
- C) To account for negative values in the image
- D) To amplify small differences between regions
  **Answer: A**

### 18. When would a normalized correlation value be exactly 1?

- A) When the template and image region are identical in shape but may differ in brightness
- B) When the template and image region are completely different
- C) When the template is all zeros
- D) When the image region is brighter than the template
  **Answer: A**

### 19. How does template matching using correlation handle image regions of different brightness compared to the template?

- A) Standard correlation fails, but normalized correlation works well
- B) Both standard and normalized correlation fail
- C) Standard correlation works well, but normalized correlation fails
- D) Both work equally well regardless of brightness differences
  **Answer: A**

### 20. The computational complexity of performing correlation on an image of size M×N with a filter of size K×L is:

- A) O(M×N)
- B) O(K×L)
- C) O(M×N×K×L)
- D) O(M+N+K+L)
  **Answer: C**

## True/False Questions (10)

### 1. Correlation and convolution produce identical results when the kernel is symmetrical.

- True
- False
  **Answer: True**

### 2. Template matching using correlation works well even when the pattern in the image is rotated relative to the template.

- True
- False
  **Answer: False**

### 3. In normalized correlation, the result is always in the range [-1, 1].

- True
- False
  **Answer: True**

### 4. When performing 2D correlation, the minimum required padding depends only on the size of the filter.

- True
- False
  **Answer: True**

### 5. Convolving a function with a delta (unit impulse) function always produces a scaled version of the original function.

- True
- False
  **Answer: False**

### 6. The dot product between two vectors achieves its maximum value when the vectors are perpendicular to each other.

- True
- False
  **Answer: False**

### 7. In template matching, normalized correlation is invariant to both additive and multiplicative brightness changes in the image.

- True
- False
  **Answer: False**

### 8. The first value of correlation corresponds to a displacement of one unit of the filter.

- True
- False
  **Answer: False**

### 9. Correlation can be interpreted as measuring the similarity between a template and different regions of an image.

- True
- False
  **Answer: True**

### 10. In convolution, the filter is first rotated by 90° before the shift operations.

- True
- False
  **Answer: False**

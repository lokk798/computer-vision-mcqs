# Computer Vision MCQ Part 4: Image Processing

1. Which of the following transformations is most appropriate when we need to compress the dynamic range of an image with large variations in pixel values?

   - A) Gain/Bias transformation
   - B) Negative transformation
   - C) Log transformation
   - D) Linear contrast stretching

   **Correct Answer: C) Log transformation**

2. In the power law transformation s = c·r^γ, what effect does a γ > 1 have on an image?

   - A) It expands the contrast in dark regions while compressing it in bright regions
   - B) It expands the contrast in bright regions while compressing it in dark regions
   - C) It uniformly expands contrast across all intensity levels
   - D) It produces a negative image

   **Correct Answer: B) It expands the contrast in bright regions while compressing it in dark regions**

3. What is the primary purpose of histogram equalization?

   - A) To create a bimodal histogram
   - B) To make all intensity values equally likely
   - C) To normalize the image so the mean intensity value is exactly in the middle of the range
   - D) To minimize the variance between neighboring pixels

   **Correct Answer: B) To make all intensity values equally likely**

4. The spatial domain processing of an image can be described by which expression?

   - A) g(x,y) = T[f(x,y)]
   - B) g(u,v) = H(u,v)·F(u,v)
   - C) g(x,y) = T[f(a,b) where (a,b) is in the neighborhood of (x,y)]
   - D) g(x,y) = f(x,y) \* h(x,y)

   **Correct Answer: C) g(x,y) = T[f(a,b) where (a,b) is in the neighborhood of (x,y)]**

5. Which of the following properties is NOT typically associated with linear filters?

   - A) Superposition
   - B) Scaling
   - C) Shift invariance
   - D) Median preservation

   **Correct Answer: D) Median preservation**

6. For a CRT monitor with a gamma of 2.5, what gamma correction should be applied to input images to achieve a linear response?

   - A) 2.5
   - B) 1/2.5
   - C) 0.4
   - D) Both B and C

   **Correct Answer: D) Both B and C**

7. What is the result of applying a Laplacian filter to an image?

   - A) Smoothing of edges
   - B) Highlighting of edges and fine details
   - C) Color correction
   - D) Uniform contrast enhancement

   **Correct Answer: B) Highlighting of edges and fine details**

8. Which filter type would be most effective for removing salt-and-pepper noise while preserving edges?

   - A) Gaussian filter
   - B) Average filter
   - C) Median filter
   - D) Laplacian filter

   **Correct Answer: C) Median filter**

9. In the process of unsharp masking, what is the "mask" referred to?

   - A) The original image
   - B) The blurred version of the original image
   - C) The difference between the original and blurred image
   - D) The final sharpened result

   **Correct Answer: C) The difference between the original and blurred image**

10. If a 3×3 average filter is applied to an image containing sharp transitions, what will happen to these transitions?

    - A) They will become more pronounced
    - B) They will be blurred
    - C) They will be completely removed
    - D) They will remain unchanged

    **Correct Answer: B) They will be blurred**

11. The bilateral filter differs from the Gaussian filter primarily because it:

    - A) Operates in the frequency domain instead of the spatial domain
    - B) Considers both spatial proximity and intensity similarity
    - C) Uses median values instead of weighted averages
    - D) Applies only to color images

    **Correct Answer: B) Considers both spatial proximity and intensity similarity**

12. For log transformation s = c·log(1+r), how is the constant c typically chosen for an 8-bit image?

    - A) c = 255
    - B) c = 255/log(1+255)
    - C) c = log(1+255)
    - D) c = 255/log(255)

    **Correct Answer: B) c = 255/log(1+255)**

13. What characteristic makes the Laplacian operator an isotropic second-order derivative operator?

    - A) It detects edges only in horizontal and vertical directions
    - B) It behaves the same in all directions
    - C) It has zero-sum coefficients
    - D) It uses absolute values of differences

    **Correct Answer: B) It behaves the same in all directions**

14. In Otsu thresholding, what criterion is used to determine the optimal threshold value?

    - A) Maximizing the between-class variance
    - B) Minimizing the within-class variance
    - C) Both A and B (they are equivalent)
    - D) Equalizing the number of pixels in each class

    **Correct Answer: C) Both A and B (they are equivalent)**

15. The α-trimmed mean filter with α = 0 is equivalent to which of the following filters?

    - A) Median filter
    - B) Max filter
    - C) Min filter
    - D) Arithmetic mean filter

    **Correct Answer: D) Arithmetic mean filter**

16. What is the kernel matrix for a 3×3 Laplacian filter that includes diagonal directions?

    - A) [[-1,-1,-1],[-1,8,-1],[-1,-1,-1]]
    - B) [[0,1,0],[1,-4,1],[0,1,0]]
    - C) [[1,1,1],[1,-8,1],[1,1,1]]
    - D) [[1,2,1],[2,-12,2],[1,2,1]]

    **Correct Answer: A) [[-1,-1,-1],[-1,8,-1],[-1,-1,-1]]**

17. When implementing a Gaussian filter, what effect does increasing σ have?

    - A) Decreases the amount of smoothing
    - B) Increases the amount of smoothing
    - C) Makes the filter more sensitive to edges
    - D) Has no effect on the smoothing, only on the computational efficiency

    **Correct Answer: B) Increases the amount of smoothing**

18. In contrast enhancement using piecewise-linear functions, what shape is typically used?

    - A) Linear
    - B) Exponential
    - C) Sigmoid
    - D) Hyperbolic

    **Correct Answer: C) Sigmoid**

19. For an image with histogram concentrated in the middle range of intensities, which transformation would be most effective for enhancing contrast?

    - A) Negative transformation
    - B) Log transformation
    - C) Contrast stretching
    - D) Threshold transformation

    **Correct Answer: C) Contrast stretching**

20. The first-order derivative of a digital image typically produces:

    - A) Single pixel thick edges
    - B) Thick edges
    - C) Double edges separated by zeros
    - D) No visible edges at all

    **Correct Answer: B) Thick edges**

## True/False Questions

1. In a log transformation, the constant c is chosen to ensure that the maximum input value maps to the maximum output value.

   - True
   - False

   **Correct Answer: True**

2. The Laplacian operator is an example of a first-order derivative filter.

   - True
   - False

   **Correct Answer: False** (It's a second-order derivative operator)

3. When applying a 5×5 average filter to an image, the filter coefficients must sum to 1 to maintain the same average brightness level.

   - True
   - False

   **Correct Answer: True**

4. The negative transformation is equivalent to a power law transformation with γ = -1.

   - True
   - False

   **Correct Answer: False** (Negative transformation is s = L-1-r, not r^(-1))

5. The second-order derivative of a digital image produces double edges that are separated by zeros.

   - True
   - False

   **Correct Answer: True**

6. A median filter with a window size of 3×3 will always preserve sharp edges in the image.

   - True
   - False

   **Correct Answer: False** (It preserves edges better than linear filters, but doesn't always preserve all edges perfectly)

7. In histogram equalization, the resulting histogram is always perfectly uniform.

   - True
   - False

   **Correct Answer: False** (Due to the discrete nature of digital images, the result is usually an approximation of a uniform distribution)

8. The bilateral filter can be implemented as a convolution operation with a fixed kernel.

   - True
   - False

   **Correct Answer: False** (It's non-linear because the weights depend on the image content)

9. Applying a Gaussian filter with σ = 0 is equivalent to not filtering the image at all.

   - True
   - False

   **Correct Answer: True**

10. Otsu thresholding works best when the image histogram has a bimodal distribution.

    - True
    - False

    **Correct Answer: True**

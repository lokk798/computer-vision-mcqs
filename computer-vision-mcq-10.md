# Part 10

# RANSAC Algorithm - Challenging Quiz Questions

## Multiple Choice Questions (MCQ)

### Question 1

In the RANSAC algorithm, what is the primary reason for adding step 6 (fitting the model to the final consensus set) after selecting the model with the largest consensus set?

- a) To reduce computational complexity of subsequent iterations
- b) To improve the model quality by using all identified inliers rather than just the minimal sample
- c) To verify that the consensus set is actually composed of true inliers
- d) To calculate the final error threshold for the model

**Correct Answer: b**

### Question 2

Given the RANSAC iteration formula N = log(1-p)/log(1-(1-e)^s), if the outlier ratio e = 0.5, minimum points s = 4, and desired probability p = 0.99, approximately how many iterations are needed?

- a) 17 iterations
- b) 35 iterations
- c) 72 iterations
- d) 146 iterations

**Correct Answer: c**

### Question 3

According to the lecture's iteration table, what happens to the required number of RANSAC iterations when the outlier ratio increases from 0.1 to 0.5 for s=3 and p=0.99?

- a) Iterations increase by a factor of approximately 2
- b) Iterations increase by a factor of approximately 3
- c) Iterations increase by a factor of approximately 8
- d) Iterations remain approximately the same

**Correct Answer: c**

### Question 4

In the visual demonstration showing consensus sets of size 4 and 13, what would be the most likely reason the algorithm would prefer the model with 13 inliers over the one with 4 inliers?

- a) The model with 13 inliers has lower computational cost
- b) The model with 4 inliers is more likely to be affected by noise
- c) The larger consensus set indicates better model generalization to the data
- d) Models with fewer inliers are always considered outliers themselves

**Correct Answer: c**

### Question 5

Why does RANSAC work particularly well when s ∈ [1...10] according to the lecture?

- a) Because larger values of s make the algorithm too slow
- b) Because the probability of selecting all inliers decreases exponentially with s
- c) Because models requiring more than 10 points are inherently unstable
- d) Because the consensus scoring becomes unreliable for larger s values

**Correct Answer: b**

### Question 6

Which statement best explains why RANSAC is described as "not good for getting multiple fits"?

- a) The algorithm always stops after finding the first acceptable model
- b) The random sampling approach cannot distinguish between different valid models in the data
- c) Multiple models would require exponentially more iterations
- d) The consensus mechanism inherently favors single global solutions over multiple local ones

**Correct Answer: d**

### Question 7

In homography estimation using RANSAC, what would be the minimum value of s (minimum points needed)?

- a) 2 points (one correspondence)
- b) 3 points (minimum for perspective transformation)
- c) 4 points (minimum for full homography matrix)
- d) 8 points (for overdetermined system)

**Correct Answer: c**

### Question 8

Based on the iteration tables provided, what can be concluded about the relationship between required confidence level p and computational efficiency?

- a) Higher confidence always requires exponentially more iterations
- b) The iteration count is linear with respect to confidence level
- c) Confidence level has minimal impact compared to outlier ratio
- d) There's a practical trade-off where very high confidence becomes computationally prohibitive

**Correct Answer: d**

### Question 9

In the context of the PnP (Perspective-n-Point) problem mentioned in applications, what makes RANSAC particularly suitable compared to least squares fitting?

- a) RANSAC can work with fewer point correspondences
- b) RANSAC is inherently faster for pose estimation
- c) RANSAC can handle incorrect feature matches that would corrupt least squares solutions
- d) RANSAC provides more accurate camera calibration parameters

**Correct Answer: c**

### Question 10

According to the lecture, RANSAC can handle "up to 50%" outliers. What happens to the algorithm's effectiveness as the outlier ratio approaches this limit?

- a) The algorithm becomes more accurate due to better outlier detection
- b) Computational requirements grow dramatically while success probability drops
- c) The minimum sample size s must be increased proportionally
- d) The consensus threshold must be made more restrictive

**Correct Answer: b**

---

## True/False Questions

### Question 1

**Statement:** In RANSAC, the "consensus set" refers to the randomly selected subset of points used to initially fit the model in each iteration.

**Answer: False**

**Explanation:** The consensus set refers to ALL data points (including the initial hypothetical inliers) that are classified as inliers when tested against the fitted model. The randomly selected subset is called "hypothetical inliers," while the consensus set is the complete set of points that fit the model within the specified threshold.

### Question 2

**Statement:** According to the RANSAC iteration formula, if you need 99.9% confidence (p=0.999) instead of 99% confidence (p=0.99), you approximately need to double the number of iterations regardless of the outlier ratio.

**Answer: False**

**Explanation:** The relationship is not linear. Looking at the tables, for s=4 and e=0.5, going from p=0.99 (72 iterations) to p=0.999 (108 iterations) is about 1.5x increase, not 2x. The exact ratio depends on both the outlier ratio e and minimum sample size s, as the formula involves logarithmic relationships.

### Question 3

**Statement:** The main advantage of using a smaller minimum sample size s in RANSAC is that it requires fewer iterations, but this comes at the cost of potentially less stable model fitting.

**Answer: False**

**Explanation:** While it's true that smaller s requires fewer iterations (making RANSAC more efficient), it doesn't necessarily result in less stable model fitting. The stability depends on the nature of the problem and the model being fitted. For some applications, smaller s can actually lead to more robust results by being less sensitive to outliers in the initial sample.

### Question 4

**Statement:** In the visual example where one iteration produces 4 inliers and another produces 13 inliers, RANSAC would automatically select the model with 13 inliers as the final result without considering any other factors.

**Answer: False**

**Explanation:** While RANSAC selects the model with the largest consensus set, the algorithm continues for a predetermined number of iterations N before making the final selection. The model with 13 inliers would only be selected if it remains the largest consensus set after all N iterations are completed. Additionally, some implementations might consider other factors like model quality metrics in case of ties.

### Question 5

**Statement:** The reason RANSAC is particularly effective for homography estimation in panorama stitching is because it can simultaneously detect and ignore incorrect feature matches between images.

**Answer: True**

**Explanation:** This statement is correct. In panorama stitching, feature matching algorithms often produce incorrect correspondences between images due to repetitive textures, noise, or similar-looking features. RANSAC excels in this application because it can identify the correct geometric transformation (homography) while automatically treating incorrect matches as outliers, making it robust to the high percentage of wrong correspondences typical in feature matching scenarios.

# Part 16

# Computer Vision Deep Learning Quiz

## Tricky MCQ and True/False Questions

---

## Multiple Choice Questions (MCQs)

### Question 1

In object localization, when the output vector y contains [Pc, bx, by, bw, bh, c1, c2, c3], what happens to the bounding box parameters when Pc = 0?

- A) The bounding box parameters are set to zero
- B) The bounding box parameters are ignored during loss calculation
- C) The bounding box parameters are still used for training
- D) The bounding box parameters become don't care values (?)

**Answer: D**

### Question 2

In the sliding window approach for object detection, what is the primary advantage of converting fully connected layers to convolutional layers?

- A) It reduces the number of parameters in the model
- B) It allows processing multiple window positions simultaneously in one forward pass
- C) It improves the accuracy of detection
- D) It eliminates the need for sliding windows entirely

**Answer: B**

### Question 3

According to the lecture, what IoU threshold is considered indicative of "good detection"?

- A) IoU > 0.3
- B) IoU > 0.4
- C) IoU > 0.5
- D) IoU > 0.7

**Answer: C**

### Question 4

In the non-max suppression algorithm described, what is the first step after discarding predictions with p < 0.6?

- A) Calculate IoU for all remaining boxes
- B) Pick the box with the highest value of p
- C) Sort all boxes by their bounding box area
- D) Remove boxes with overlapping coordinates

**Answer: B**

### Question 5

What is the main limitation of the basic object detection approach (without anchor boxes) mentioned in the lecture?

- A) It cannot detect small objects
- B) Each grid cell can detect only one object
- C) It requires too much computational power
- D) It cannot classify multiple object types

**Answer: B**

### Question 6

In YOLO's anchor box design using k-means clustering, what distance metric is used instead of Euclidean distance?

- A) Manhattan distance
- B) Cosine distance
- C) IoU-based distance metric
- D) Hamming distance

**Answer: C**

### Question 7

When using anchor boxes, how are ground truth boxes matched to anchors during training?

- A) By minimizing the Euclidean distance between box centers
- B) By maximizing the overlap area
- C) By matching to the closest anchors using IoU
- D) By random assignment to available anchors

**Answer: C**

### Question 8

In landmark detection as shown in the lecture example, how many coordinate pairs are used for face landmark detection?

- A) 32 pairs (64 values)
- B) 64 pairs (128 values)
- C) 68 pairs (136 values)
- D) 64 individual coordinates

**Answer: A**

### Question 9

What happens during the convolutional sliding window when the input changes from 16×16×3 to a larger image?

- A) The network needs to be retrained
- B) Multiple predictions are generated simultaneously across different positions
- C) The accuracy decreases significantly
- D) Only the center region is processed

**Answer: B**

### Question 10

In the non-max suppression algorithm, after picking the box with highest p value, what IoU threshold is used to discard overlapping boxes?

- A) IoU > 0.3
- B) IoU > 0.4
- C) IoU > 0.5
- D) IoU > 0.6

**Answer: C**

---

## True/False Questions

### Question 1

**Statement:** In object localization, when there is no object present in the image (background class), the bounding box parameters (bx, by, bw, bh) should be set to zero in the training data.

**Answer: False**

**Explanation:** When Pc = 0 (no object present), the bounding box parameters become "don't care" values (represented as ? in the lecture). They are not set to zero but rather ignored during loss calculation since there's no object to localize. Setting them to zero would imply a specific bounding box location, which is meaningless when no object exists.

### Question 2

**Statement:** The sliding window approach becomes computationally efficient only after converting fully connected layers to convolutional layers because it reduces the total number of parameters in the network.

**Answer: False**

**Explanation:** Converting FC layers to convolutional layers doesn't reduce the number of parameters - it maintains the same parameters but reshapes them as convolution kernels. The computational efficiency comes from being able to process multiple sliding window positions simultaneously in a single forward pass, rather than running separate forward passes for each window position.

### Question 3

**Statement:** In the non-max suppression algorithm, if two bounding boxes have IoU > 0.5, the box with the lower confidence score is always discarded, regardless of which classes they detect.

**Answer: False**

**Explanation:** This statement is tricky because while NMS does discard boxes with lower confidence when IoU > 0.5, it's typically applied per class. Two boxes detecting different classes might both be kept even if they overlap significantly, as they represent different object detections. The algorithm shown in the lecture appears to be for single-class detection.

### Question 4

**Statement:** Anchor boxes solve the limitation of detecting only one object per grid cell by allowing each grid cell to output multiple bounding box predictions with different aspect ratios and scales.

**Answer: True**

**Explanation:** This is correct. Anchor boxes enable each grid cell to detect multiple objects by providing multiple "templates" of different shapes and sizes. Each anchor box can detect one object, so with multiple anchor boxes per grid cell, multiple objects can be detected in the same spatial region.

### Question 5

**Statement:** In YOLO's k-means clustering for anchor box design, using IoU-based distance instead of Euclidean distance ensures that the resulting anchor boxes are optimized for better overlap with ground truth boxes rather than just similar dimensions.

**Answer: True**

**Explanation:** This is correct and quite insightful. IoU-based distance considers how well boxes would overlap regardless of their absolute positions, which is more relevant for object detection than Euclidean distance between width-height pairs. This leads to anchor boxes that are better suited for the actual shapes of objects in the dataset, improving detection performance.

# Part 15

# Motion Analysis - Computer Vision Quiz

## Multiple Choice Questions (MCQs)

### Question 1

In the Lucas-Kanade optical flow method, what is the primary reason why a pyramidal approach is often necessary?

- A) To reduce computational complexity by processing fewer pixels
- B) To handle the aperture problem more effectively
- C) To overcome the small displacement assumption limitation
- D) To improve brightness constancy in different lighting conditions

**Correct Answer: C**

### Question 2

When comparing Horn-Schunck and Lucas-Kanade methods, which statement best describes their fundamental difference in handling motion estimation?

- A) Horn-Schunck uses local patches while Lucas-Kanade uses global optimization
- B) Lucas-Kanade assumes constant velocity locally while Horn-Schunck enforces global smoothness
- C) Horn-Schunck is faster because it uses fewer iterations
- D) Lucas-Kanade handles occlusions better due to its global approach

**Correct Answer: B**

### Question 3

In discriminative correlation filters (like MOSSE), what is the key advantage over traditional template matching using simple correlation?

- A) They use FFT for faster computation
- B) They create a desired response pattern during training rather than just matching templates
- C) They work better with color information
- D) They require less memory for storing templates

**Correct Answer: B**

### Question 4

The Mean-Shift tracking algorithm uses color histograms and Bhattacharyya distance. What is the main limitation of this approach?

- A) It cannot handle fast motion
- B) It's computationally too expensive for real-time applications
- C) It lacks spatial information and can track similar colored objects incorrectly
- D) It requires manual initialization of the number of histogram bins

**Correct Answer: C**

### Question 5

In the context of deep learning for tracking (like MDNet), what is the purpose of "hard negative mining"?

- A) To reduce the number of training samples for faster convergence
- B) To select the most difficult negative samples that the model struggles with
- C) To prevent overfitting by removing easy negative samples
- D) To balance the dataset by removing redundant negative samples

**Correct Answer: B**

### Question 6

The SiamFC tracker uses a fully convolutional Siamese network. What is the main trade-off of not updating the template during tracking?

- A) Higher computational cost but better accuracy
- B) Lower accuracy in long sequences but faster processing and no drift
- C) Better handling of occlusions but worse scale estimation
- D) Improved robustness to illumination changes but worse motion handling

**Correct Answer: B**

### Question 7

In multi-object tracking using tracking-by-detection, what is the primary challenge that offline tracking methods attempt to solve?

- A) Reducing computational complexity of the detection step
- B) Improving the accuracy of individual object detectors
- C) Handling missing detections and maintaining global trajectory consistency
- D) Reducing memory requirements for storing multiple object templates

**Correct Answer: C**

### Question 8

When using Histogram of Oriented Gradients (HOG) features in tracking (like KCF), why are they preferred over raw intensity values?

- A) They require less memory storage
- B) They are invariant to illumination changes and provide structural information
- C) They can be computed faster using integral images
- D) They work better with circular correlation in Fourier domain

**Correct Answer: B**

### Question 9

In the context of the aperture problem in optical flow, which scenario would be most affected?

- A) A textured object moving diagonally
- B) A plain white rectangle moving horizontally
- C) A rotating circular object with radial patterns
- D) A checkerboard pattern moving in any direction

**Correct Answer: B**

### Question 10

The incremental PCA approach in IVT (Incremental Visual Tracking) addresses which fundamental challenge in appearance-based tracking?

- A) Reducing computational complexity of feature extraction
- B) Handling gradual appearance changes while maintaining a compact model
- C) Improving the initial template selection process
- D) Enabling real-time performance through parallel processing

**Correct Answer: B**

## True/False Questions

### Question 1

**Statement:** In optical flow estimation, the brightness constancy assumption means that pixel intensities remain exactly the same between consecutive frames.

**Answer: False**

**Explanation:** The brightness constancy assumption states that the brightness of a moving point remains _approximately_ constant between frames, not exactly the same. This is a fundamental assumption that allows optical flow algorithms to work, but it's often violated in practice due to lighting changes, shadows, reflections, and other factors. The assumption is that I(x,y,t) = I(x+dx, y+dy, t+dt), but this is only an approximation.

### Question 2

**Statement:** The main advantage of using deep learning approaches for optical flow (like FlowNet and RAFT) over traditional methods is that they can be trained on synthetic data and still generalize well to real-world scenarios.

**Answer: True**

**Explanation:** This is indeed one of the key advantages highlighted in the lecture. Deep learning methods for optical flow can be effectively trained on synthetic datasets (where ground truth flow is known) and then generalize to real-world data. This overcomes the challenge of obtaining ground truth optical flow for real videos, which is extremely difficult or impossible to measure directly.

### Question 3

**Statement:** In correlation-based tracking, applying a Hanning window is primarily used to improve the speed of FFT computation.

**Answer: False**

**Explanation:** The Hanning window is applied to address the boundary effects caused by the circular nature of correlation in the Fourier domain, not to improve FFT speed. When computing correlation via FFT, the operation becomes circular, which can cause artifacts at the boundaries. The Hanning window helps mitigate these circular boundary effects by gradually reducing the signal to zero at the edges.

### Question 4

**Statement:** In single-object tracking, discriminative models generally require more training data than generative models because they need to learn the differences between the target and background.

**Answer: False**

**Explanation:** According to the lecture, discriminative models actually require _less_ data than generative models. Discriminative models focus on learning the decision boundary between target and background (which requires fewer examples), while generative models need to model the entire appearance distribution of the object (which requires more comprehensive data to capture all possible variations).

### Question 5

**Statement:** The KCF (Kernelized Correlation Filter) tracker uses separate filters for different HOG channels and then averages their responses to get the final tracking result.

**Answer: True**

**Explanation:** The lecture specifically mentions that KCF uses a "multichannel formulation (HOG)" with "separate filters" that produce "separate responses" which are then combined through an "average response." This approach allows KCF to leverage the rich information from different HOG channels while maintaining the efficiency of correlation filter-based tracking.</content>
</invoke>

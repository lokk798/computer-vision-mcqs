# Part 6: Image Filtering in the Frequency Domain - MCQ and True/False Questions

## Multiple Choice Questions

1. What was Fourier initially studying that led him to develop the Fourier transform?

   - Heat propagation through materials
   - Light refraction
   - Sound waves
   - Electrical circuits

   **Correct Answer:** Heat propagation through materials

2. The Fourier transform represents a signal f(x) in terms of:

   - Spatial variations and their gradients
   - Peak values and their dispersions
   - Amplitudes and phases of constituent sinusoids
   - Wavelets and their coefficients

   **Correct Answer:** Amplitudes and phases of constituent sinusoids

3. In the formula for a sinusoid f(x) = A sin(2πux + φ), what does 'u' represent?

   - Phase shift
   - Wave amplitude
   - Frequency
   - Time period

   **Correct Answer:** Frequency

4. The mathematical relationship e^(iθ) = cos(θ) + i sin(θ) is explained in the document using:

   - Trigonometric substitution
   - Euler's identity
   - Taylor series expansion
   - Integration by parts

   **Correct Answer:** Taylor series expansion

5. According to the convolution theorem, if g(x) = f(x) \* h(x), then G(u) equals:

   - F(u) + H(u)
   - F(u) \* H(u)
   - F(u) / H(u)
   - F(u) × H(u)

   **Correct Answer:** F(u) × H(u)

6. What is the effect of a low-pass filter on an image?

   - Enhances edges and fine details
   - Increases contrast
   - Blurs the image
   - Removes color information

   **Correct Answer:** Blurs the image

7. High frequencies in the Fourier transform of an image correspond to:

   - Slowly varying intensity components
   - Uniform brightness regions
   - Sharp transitions like edges and corners
   - Overall image contrast

   **Correct Answer:** Sharp transitions like edges and corners

8. The cut-off frequency in a filter refers to:

   - The maximum frequency that can be represented in a digital image
   - The point of transition between H(u,v) = 1 and H(u,v) = 0
   - The sampling rate of the image
   - The frequency at which noise becomes dominant

   **Correct Answer:** The point of transition between H(u,v) = 1 and H(u,v) = 0

9. What differentiates the Butterworth filter from the Ideal filter?

   - Butterworth filter has a gradual transition between passed and filtered frequencies
   - Butterworth filter only works on color images
   - Butterworth filter requires less computational power
   - Butterworth filter can only be applied in the spatial domain

   **Correct Answer:** Butterworth filter has a gradual transition between passed and filtered frequencies

10. In hybrid images, what technique is used to combine two images?

    - One image is processed with a high-pass filter and another with a low-pass filter, then combined
    - Both images are processed with band-pass filters of different frequencies
    - One image provides the phase information and another provides the magnitude
    - Both images are converted to grayscale and then averaged

    **Correct Answer:** One image is processed with a high-pass filter and another with a low-pass filter, then combined

11. What is the formula for the Butterworth Low-pass filter of order n and cutoff frequency D₀?

    - H(u,v) = 1 / (1 + [D(u,v)/D₀]²ⁿ)
    - H(u,v) = 1 / (1 + [D₀/D(u,v)]²ⁿ)
    - H(u,v) = 1 - 1 / (1 + [D(u,v)/D₀]²ⁿ)
    - H(u,v) = 1 - e^(-D(u,v)²/2D₀²)

    **Correct Answer:** H(u,v) = 1 / (1 + [D(u,v)/D₀]²ⁿ)

12. When reconstructing an image using only phase information from the Fourier transform:

    - The result is completely unrecognizable
    - The spatial layout of the image is preserved but intensity values are lost
    - Only the high-frequency components are preserved
    - The result contains no visual information

    **Correct Answer:** The spatial layout of the image is preserved but intensity values are lost

13. What happens when all phase values in a Fourier transform are set to zero while preserving the magnitude?

    - The image becomes completely black
    - The image becomes completely white
    - The reconstructed image loses most of its distinct features
    - The reconstructed image has enhanced edges

    **Correct Answer:** The reconstructed image loses most of its distinct features

14. The 2D Discrete Fourier Transform (DFT) of an M×N image produces:

    - An M×N complex-valued result
    - An M×N real-valued result
    - A single complex number
    - A 1D array of length M+N

    **Correct Answer:** An M×N complex-valued result

15. In the equation F(u) = ℜ[F(u)] + i ℑ[F(u)] = A(u)e^(iφ(u)), how is the amplitude A(u) calculated?

    - A(u) = √(ℜ[F(u)]² + ℑ[F(u)]²)
    - A(u) = ℜ[F(u)] + ℑ[F(u)]
    - A(u) = max(ℜ[F(u)], ℑ[F(u)])
    - A(u) = |ℜ[F(u)] - ℑ[F(u)]|

    **Correct Answer:** A(u) = √(ℜ[F(u)]² + ℑ[F(u)]²)

16. According to the document, what was the impact of the fast Fourier transform (FFT) algorithm discovery in the early 1960s?

    - It revolutionized the field of signal processing
    - It enabled the first digital camera
    - It made possible the compression of audio signals
    - It led to the development of medical imaging

    **Correct Answer:** It revolutionized the field of signal processing

17. When visualizing the Fourier transform of an image, what transformation is typically applied to make the values more visible?

    - Square root
    - Logarithm
    - Exponential
    - Sine

    **Correct Answer:** Logarithm

18. In the context of image processing, what is the relationship between filtering in the spatial domain and in the frequency domain?

    - Convolution in the spatial domain corresponds to multiplication in the frequency domain
    - Convolution in the spatial domain corresponds to division in the frequency domain
    - Convolution in the spatial domain corresponds to addition in the frequency domain
    - Convolution in the spatial domain corresponds to integration in the frequency domain

    **Correct Answer:** Convolution in the spatial domain corresponds to multiplication in the frequency domain

19. What is the main advantage of performing filtering in the frequency domain rather than in the spatial domain?

    - It is more computationally efficient for large filters
    - It allows for color processing
    - It preserves the edges better
    - It reduces memory usage

    **Correct Answer:** It is more computationally efficient for large filters

20. Which component of the Fourier transform carries most of the information about where discernible objects are located in an image?

    - Magnitude
    - Phase
    - Real part
    - Imaginary part

    **Correct Answer:** Phase

## True/False Questions

1. - The Fast Fourier Transform (FFT) algorithm was discovered in the early 1950s.
     **False** (It was discovered in the early 1960s)

2. - In the Fourier transform of an image, low frequencies represent slowly varying intensity components.
     **True**

3. - A high-pass filter enhances sharp details but increases the overall contrast of an image.
     **False** (It causes a reduction in contrast)

4. - The phase component of the Fourier transform is generally less important than the magnitude for preserving visual information.
     **False** (The phase is often more important)

5. - The Butterworth filter and the Ideal filter produce identical results when applied to an image.
     **False** (They produce different results due to different transition characteristics)

6. - Convolving a signal with a Gaussian kernel in the spatial domain is equivalent to multiplying its Fourier transform by the Fourier transform of the Gaussian kernel.
     **True**

7. - Hybrid images combine a low-pass filtered version of one image with a band-pass filtered version of another image.
     **False** (They combine a low-pass filtered version of one image with a high-pass filtered version of another)

8. - The Fourier transform of a real-valued image is always real-valued.
     **False** (It is generally complex-valued)

9. - According to the convolution theorem, convolution in the spatial domain corresponds to multiplication in the frequency domain.
     **True**

10. - When reconstructing an image using only amplitude information from its Fourier transform, the result will contain all the distinct features of the original image.
      **False** (Much of the spatial information is lost without phase)

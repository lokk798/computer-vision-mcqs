# Computer Vision MCQ Part 2

## Question 1

Which of the following statements about light is incorrect?

- Light can reflect off mirrors and cast shadows
- Light behaves like a particle (photon) and has mass
- Light can refract when passing from one medium to another
- Light can diffract when passing through a narrow slit

**Correct Answer**: Light behaves like a particle (photon) and has mass

## Question 2

What occurs during the refraction of light?

- Light changes direction as it passes from one medium to another due to a change in speed
- Light bends around obstacles or spreads out after passing through a narrow slit
- Light is absorbed and re-emitted by a surface
- Light changes its wavelength without changing direction

**Correct Answer**: Light changes direction as it passes from one medium to another due to a change in speed

## Question 3

What determines the colors that humans perceive in an object?

- The temperature of the object
- The density of the object
- The nature of light reflected from the object
- The size of the object

**Correct Answer**: The nature of light reflected from the object

## Question 4

What is the BRDF (Bidirectional Reflectance Distribution Function) used for in computer vision?

- To model how light is scattered and reflected when it hits a surface
- To calculate the focal length of a camera lens
- To determine the minimum aperture size for a pinhole camera
- To measure the wavelength of visible light

**Correct Answer**: To model how light is scattered and reflected when it hits a surface

## Question 5

What is the primary limitation of using a very small pinhole in a camera obscura?

- It allows too much light to enter, overexposing the image
- It causes diffraction effects that decrease image sharpness
- It inverts the image horizontally rather than vertically
- It can only capture black and white images

**Correct Answer**: It causes diffraction effects that decrease image sharpness

## Question 6

In the digital image sensing process, what is the main difference between CCD and CMOS sensors regarding A/D conversion?

- CCDs convert analog signals at the end of each row/column, while CMOS converts directly at each sensing cell
- CCDs use binary conversion while CMOS uses hexadecimal
- CCDs convert all signals simultaneously while CMOS converts sequentially
- CCDs require external conversion while CMOS has no conversion capability

**Correct Answer**: CCDs convert analog signals at the end of each row/column, while CMOS converts directly at each sensing cell

## Question 7

Which statement about brightness is most accurate?

- Brightness is an objective measurement of light intensity
- Brightness is equivalent to luminance in all contexts
- Brightness is a subjective descriptor of light intensity
- Brightness is measured in wavelength units

**Correct Answer**: Brightness is a subjective descriptor of light intensity

## Question 8

What mathematical representation is commonly used to model a digital image?

- A function I: Ω ⊂ ℝ² → ℝ, where the domain is a subset of the real image plane
- A vector field with constant magnitude
- A probability distribution function of light waves
- A complex number representing amplitude and phase

**Correct Answer**: A function I: Ω ⊂ ℝ² → ℝ, where the domain is a subset of the real image plane

## Question 9

In the process of converting a continuous image to a digital one, what is quantization responsible for?

- Reducing the image domain to a finite set of spatial coordinates
- Increasing the dynamic range of the image
- Reducing the sensor response to a finite set of values
- Expanding the color spectrum

**Correct Answer**: Reducing the sensor response to a finite set of values

## Question 10

What is the approximate dynamic range of the human eye?

- 10³
- 10⁶
- 10⁹
- 10¹²

**Correct Answer**: 10⁹

## Question 11

When discussing image resolution, which pair of parameters defines the spatial resolution?

- The intensity values and contrast
- The number of bits per pixel and quantization levels
- The matrix dimensions M and N
- The focal length and aperture size

**Correct Answer**: The matrix dimensions M and N

## Question 12

What happens when the aperture of a pinhole camera is too large?

- The image becomes sharper
- Rays from different parts of the scene mix up, causing blurring
- The image appears upright instead of inverted
- The colors in the image become more saturated

**Correct Answer**: Rays from different parts of the scene mix up, causing blurring

## Question 13

How is contrast different from dynamic range in digital imaging?

- Contrast refers to the ratio of maximum measurable intensity to minimum detectable intensity in a system, while dynamic range is the difference between highest and lowest intensity levels in an image
- Dynamic range refers to the ratio of maximum measurable intensity to minimum detectable intensity in a system, while contrast is the difference between highest and lowest intensity levels in an image
- Contrast is always measured in bits, while dynamic range is measured in pixels
- They are different terms for the same concept

**Correct Answer**: Dynamic range refers to the ratio of maximum measurable intensity to minimum detectable intensity in a system, while contrast is the difference between highest and lowest intensity levels in an image

## Question 14

Which of the following is NOT a key factor in determining how small a pinhole should be in a camera obscura?

- Diffraction effects at very small apertures
- Amount of light passing through (exposure time)
- The wavelength of the incoming light
- The material of the barrier containing the pinhole

**Correct Answer**: The material of the barrier containing the pinhole

## Question 15

What happens during the sampling process when converting a continuous image to a digital one?

- The image colors are altered to match a predefined palette
- The continuous image domain is reduced to a finite set of spatial coordinates
- The image is compressed to reduce storage requirements
- The brightness levels are adjusted to enhance contrast

**Correct Answer**: The continuous image domain is reduced to a finite set of spatial coordinates

## Question 16

Which statement is TRUE regarding spatial resolution?

- Stating that an image is 1024x1024 pixels completely defines its spatial resolution
- Spatial resolution must be stated with respect to spatial units to be meaningful
- Spatial resolution is primarily determined by the number of intensity levels
- Spatial resolution is independent of the distance to the subject

**Correct Answer**: Spatial resolution must be stated with respect to spatial units to be meaningful

## Question 17

According to the text, which sensor type works better in low light conditions?

- CMOS
- CCD
- Both work equally well
- Neither works well in low light

**Correct Answer**: CCD

## Question 18

What was the key innovation of the camera obscura compared to earlier attempts at imaging devices?

- It used digital sensors
- It incorporated glass lenses
- It placed a barrier with a small hole between the object and the sensor
- It allowed for color photography

**Correct Answer**: It placed a barrier with a small hole between the object and the sensor

## Question 19

When discussing digital images, what does intensity resolution relate to?

- The pixel density of the camera sensor
- The smallest discernible change in intensity level
- The distance at which objects can be distinguished
- The number of primary colors that can be displayed

**Correct Answer**: The smallest discernible change in intensity level

## Question 20

What is the mathematical relationship between the domain of a continuous image function and its sampled version in digital imaging?

- ℝ² → M × N, where M and N are the dimensions of the sampling grid
- ℝ → [0, 1 ... 2ᵇ - 1], where b is the bit depth
- {0,1} → [0, 255], representing binary to grayscale conversion
- ℝ³ → ℝ², representing 3D to 2D projection

**Correct Answer**: ℝ² → M × N, where M and N are the dimensions of the sampling grid

# True/False Questions

## Question 1

- A digital camera with more pixels will always produce images with better spatial resolution than a camera with fewer pixels.

**Correct Answer**: False (Spatial resolution depends not only on pixel count but also on other factors like lens quality and the distance to the subject)

## Question 2

- Quantization in digital imaging reduces the continuous range of intensity values to a finite set, while sampling reduces the continuous spatial domain to a discrete set of coordinates.

**Correct Answer**: True

## Question 3

- The pinhole in a camera obscura should be as small as technically possible to achieve the sharpest image.

**Correct Answer**: False (Making the pinhole too small causes diffraction effects which decrease image sharpness)

## Question 4

- When converting from analog to digital signals, CCD sensors typically perform the conversion at each individual sensing cell.

**Correct Answer**: False (CCD sensors perform conversion at the end of each row/column, while CMOS sensors convert at each sensing cell)

## Question 5

- A camera with 8-bit intensity resolution can represent exactly 255 different intensity levels.

**Correct Answer**: False (8-bit intensity resolution allows for 2^8 = 256 different intensity levels, ranging from 0 to 255)

## Question 6

- Light behaving as both a particle and a wave is a principle that has no practical impact on digital image formation.

**Correct Answer**: False (The wave-particle duality of light directly affects imaging, particularly through diffraction effects in small apertures)

## Question 7

- The Bidirectional Reflectance Distribution Function (BRDF) is a 5-dimensional function that models how light interacts with surfaces.

**Correct Answer**: True

## Question 8

- Brightness and luminance are objectively equivalent measurements in image processing.

**Correct Answer**: False (Brightness is a subjective descriptor of light intensity, while luminance is an objective measurement)

## Question 9

- The dynamic range of the human eye is approximately the same as that of modern digital cameras.

**Correct Answer**: False (The human eye has a dynamic range of about 10^9, which exceeds the capabilities of most standard digital cameras)

## Question 10

- In a Low Dynamic Range (LDR) image, details in both shadows and highlights are preserved equally well.

**Correct Answer**: False (LDR images lose details in either the dark areas or bright areas, unlike HDR images which preserve details in both)

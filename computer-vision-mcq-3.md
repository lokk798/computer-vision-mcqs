# Computer Vision MCQ Part 3: Color Fundamentals MCQs

## 1. Which discovery by Newton in 1660 led to the understanding that white light is composed of several colors?

- A) Reflection of light
- B) Diffraction of light
- C) Separation of white light through a prism
- D) Interference patterns of light

**Answer: C) Separation of white light through a prism**

## 2. In human vision, which type of photoreceptor cells are responsible for color vision?

- A) Rods
- B) Cones
- C) Bipolar cells
- D) Ganglion cells

**Answer: B) Cones**

## 3. What is the approximate percentage distribution of L-cones (Long-wavelength cones) in the human retina?

- A) 2-5%
- B) 32-40%
- C) 55-65%
- D) 70-80%

**Answer: C) 55-65%**

## 4. Which color matching function issue led the CIE to develop the XYZ color space?

- A) The need for device-independent colors
- B) The requirement of negative values for some red components
- C) Poor representation of yellow colors
- D) Inconsistent brightness perception

**Answer: B) The requirement of negative values for some red components**

## 5. What is a metamer in color science?

- A) A device that measures color accuracy
- B) Different combinations of wavelengths that appear identical to the human eye
- C) The maximum saturation point of a color
- D) A mathematical model for converting between color spaces

**Answer: B) Different combinations of wavelengths that appear identical to the human eye**

## 6. In the HSV color model, if V=0, what can be said about the resulting color regardless of H and S values?

- A) It will be white
- B) It will be black
- C) It will be gray
- D) It will be the pure hue with no brightness

**Answer: B) It will be black**

## 7. What is the primary advantage of the HSV color model over RGB?

- A) It can represent more colors than RGB
- B) It's more aligned with human color perception
- C) It requires less memory for storage
- D) It's directly compatible with all display technologies

**Answer: B) It's more aligned with human color perception**

## 8. In OpenCV's implementation of the HSV color model, what is the range used for the Hue component?

- A) 0 to 255
- B) 0 to 179
- C) 0 to 360
- D) -180 to 180

**Answer: B) 0 to 179**

## 9. Which of these correctly describes the S-cones in human vision?

- A) Most sensitive to red light with peak sensitivity around 560-580 nm
- B) Most sensitive to green light with peak sensitivity around 530-540 nm
- C) Most sensitive to blue light with peak sensitivity around 420-440 nm
- D) Equally sensitive to all wavelengths of visible light

**Answer: C) Most sensitive to blue light with peak sensitivity around 420-440 nm**

## 10. When converting from RGB to HSV, if R = G = B, what is the resulting Hue value?

- A) 0
- B) 360
- C) 255
- D) Undefined (as there is no dominant color)

**Answer: D) Undefined (as there is no dominant color)**

## 11. Which color model is designed specifically for printing and uses subtractive color mixing?

- A) RGB
- B) HSV
- C) CMYK
- D) YCbCr

**Answer: C) CMYK**

## 12. What makes the CIE LAB color model significant compared to RGB?

- A) It's device-independent and perceptually uniform
- B) It uses only two components instead of three
- C) It can represent infrared and ultraviolet colors
- D) It's the standard for all modern display technologies

**Answer: A) It's device-independent and perceptually uniform**

## 13. In the context of color spaces, what does the term "gamut" refer to?

- A) The mathematical formula used to convert between color spaces
- B) The range of colors that can be reproduced by a specific device or color model
- C) The precision with which colors can be represented digitally
- D) The brightness component in any color model

**Answer: B) The range of colors that can be reproduced by a specific device or color model**

## 14. What is the main difference between HSL and HSV color models in terms of brightness representation?

- A) HSL uses Lightness (midpoint between min/max RGB), while HSV uses the brightest RGB component
- B) HSL can represent more colors than HSV
- C) HSL is specific to printing, while HSV is for digital displays
- D) HSL has no brightness component

**Answer: A) HSL uses Lightness (midpoint between min/max RGB), while HSV uses the brightest RGB component**

## 15. In the RGB cube model, which coordinate represents pure white?

- A) (0, 0, 0)
- B) (1, 1, 1) or (255, 255, 255) depending on scaling
- C) (0, 0, 1) or (0, 0, 255) depending on scaling
- D) (0.5, 0.5, 0.5) or (128, 128, 128) depending on scaling

**Answer: B) (1, 1, 1) or (255, 255, 255) depending on scaling**

## 16. What is the purpose of the Ishihara Test?

- A) To calibrate digital displays
- B) To detect color blindness
- C) To measure the saturation perception of an individual
- D) To establish global color standards

**Answer: B) To detect color blindness**

## 17. Which equation correctly calculates the chromaticity coordinate x in the CIE XYZ color space?

- A) x = X / (X + Y)
- B) x = X / (X + Y + Z)
- C) x = X - Y / (X + Y + Z)
- D) x = X × Y / Z

**Answer: B) x = X / (X + Y + Z)**

## 18. In the RGB to HSV conversion, how is the chroma (C) calculated?

- A) C = V × S
- B) C = max(R,G,B) - min(R,G,B)
- C) C = (R + G + B) / 3
- D) C = √(R² + G² + B²)

**Answer: A) C = V × S**

## 19. What does the spectral locus (horseshoe shape) in the CIE 1931 chromaticity diagram represent?

- A) The range of colors visible to the human eye with maximum brightness
- B) The limits of color reproduction of all existing devices
- C) Pure spectral colors (monochromatic light)
- D) The color blindness spectrum

**Answer: C) Pure spectral colors (monochromatic light)**

## 20. Which color model component is designed specifically to correspond to the perceived relative brightness by humans?

- A) The Y component in XYZ
- B) The R component in RGB
- C) The S component in HSV
- D) The K component in CMYK

**Answer: A) The Y component in XYZ**

# True/False Questions

## 1. True or False: In the RGB color model, the combination of equal amounts of all three primary colors at maximum intensity produces black.

- True
- False

**Answer: False** (It produces white, not black)

## 2. True or False: The Y component in the YCbCr color space represents the chrominance (color) information rather than the luminance.

- True
- False

**Answer: False** (Y represents luminance, while Cb and Cr represent chrominance)

## 3. True or False: In the CIE chromaticity diagram, any color that can be created by additive mixing lies on a straight line between the two original colors.

- True
- False

**Answer: True** (Colors created by additive mixing lie on a straight line connecting the original colors on the chromaticity diagram)

## 4. True or False: The M-cones (Medium-wavelength cones) are most sensitive to red light.

- True
- False

**Answer: False** (M-cones are most sensitive to green light, while L-cones respond to red)

## 5. True or False: It's possible for two people with different types of color blindness to perceive the same color differently, while both still perceiving it as a "normal" color.

- True
- False

**Answer: True** (Different types of color blindness affect color perception in different ways)

## 6. True or False: The RGB color space is device-independent, meaning colors appear exactly the same across all devices.

- True
- False

**Answer: False** (RGB is device-dependent; the same RGB values can appear differently on different devices)

## 7. True or False: All colors perceptible by the human eye can be reproduced using the RGB color model on standard digital displays.

- True
- False

**Answer: False** (The RGB gamut is smaller than the full range of colors perceptible by humans)

## 8. True or False: In the HSV cylinder model, saturation increases as you move away from the central axis.

- True
- False

**Answer: True** (Saturation increases with distance from the central axis; the center represents zero saturation)

## 9. True or False: The K in CMYK stands for "Kelvin," referring to color temperature.

- True
- False

**Answer: False** (K stands for "Key" or black, not Kelvin)

## 10. True or False: When converting from RGB to HSV, if the saturation value is 0, the hue value becomes irrelevant because the color is a shade of gray.

- True
- False

**Answer: True** (With S=0, the color is on the grayscale axis and hue has no effect)

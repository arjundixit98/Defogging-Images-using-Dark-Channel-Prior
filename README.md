# Haze Removal

## Introduction

This is an simple implemention of "single image haze removal using dark channel prior" by kaiming He, which wins the CVPR09 best paper.

## Parameters by default
- radius=7
- omega=0.95
- t0=0.1
- r=60
- eps=0.001

## Dependencies

- numpy
- opencv-python
- skimage
- Pillow
- matplotlib
- numba

## Run

```bash
cd python_code
python haze_removal.py [your image path]
```


## References

- paper: Single Image Haze Removal using Dark Channel Prior
- paper: Guided Image Fltering
4.	PROPOSED ARCHITECTURE 
 
 
Fig(1): Overview of how Dehazing works using Dark Channel Prior 
![](images/1.jpg)
 
The proposed algorithm deals with the dehazing of images by using image degradation model and image restoration based algorithms. Firstly, we apply the Dark Channel Prior method on the image which has been taken as the input. The, apply the Fast Fourier Transform on it, which is an efficient algorithm to compute the discrete Fourier transform and is much less complicated. High pass and low pass filters are respectively used to extract high-frequency and low-frequency components from the image. Dark channel prior method is used for estimation of atmospheric light. Then, the transmission map is calculated using the spectral transform method. Then, finally the haze-free image is restored. 
 
The sequence of steps followed to produce the dehazed enhanced image are: 
•	Applying the Dark Channel Prior on the Input Image 
•	Fast Fourier Transform is then used on the Image 
•	Estimation of Atmospheric Light in the Image 
•	Refinement of the Transmission Map 
•	Refined Transmission Map together with the Atmospheric Estimated before is used to Recover the Original Image 
 

Flowchart of the proposed algorithm used: 
 
 
 
Fig(2): Flowchart of the proposed haze removal approach for visibility enhancement of single images 


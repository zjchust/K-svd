# K-svd
Image Denoising via Sparse and Redundant Representations over Learned Dictionaries


## Steps to follow for K- svd implementation
- [ ] add a fucnction which will take an image and add gaussian noise to it.
	* your function should take an clean image and a parameter say sigma and it should return a noisy image. the parameter sigma 
	will be used to vary the amount of noise to be added.
- [x] extact patches from the image
	* function should take a noisy image and dimension of patches say n and it should return a numpy matrix of dimension say(p, n*n)
- [ ] do sparse coding
	* function should initialize a dictionary and do a sparse coding. the function should return a matrix which contains sparse vectors of of the image patches. The dimension of the sparse matrix should be p X N
- [ ] update dictionary
	* this function should implement the dictionary update using the K- svd algorithm and return an updated dictionary of size 
	(N X p)

## Note 
Since this is a collaborative work, please follow the guidelines so that there is no library dependecy issues in the future.
 
* We will be using python 3.6 for our work
* Please follow pep-8 style guide. Google it and follow the instructions
* Use 4 spaces for indentation
* Add comments wherever necessary. Make your code as redable as possible.
* pull this github repo before making any commit otherwise there can be a version error.

## Runnnig the code
``` bash
python image_denoising.py -i imagename -iter 500 -coeff 2 -n_comp 100
```
## optional parameters

1. -iter: number of iterations required to learn the dictionary
2. -n_comp: number of components that the dictionary should contain
3. -coeff: number of non zero coefficients in the sparse representation of the image

## output

The output will give you 3 images, Orignal, Noisy and Reconstructed

## Results: Deep

![The above picture shows the distortion of the image Lena and its subsequent reconstruction using dictionary learning](Images/denoising.png)

The above picture shows the distortion of the image Lena and its subsequent reconstruction using dictionary learning
(a) shows the orignal image (b) shows the image after adding gaussian noise (c) Reconstructed Image




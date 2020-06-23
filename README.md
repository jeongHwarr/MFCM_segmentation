
# MFCM_segmentation (Python 3.5)
### Tissue Segmentation Using Modified Fuzzy C-Means Algorithm on Mammography (Image segmentation)

This code uses modified fuzzy c-means algorithm (MFCM) to do tissue segmentation on mammography. This code is a implementation of The paper:

[1] Z. Chen and R. Zwiggelaar, 2010. 'A Modified Fuzzy C Means Algorithm for Breast Tissue Density Segmentation in Mammograms’, IEEE/Information Technology and Applications in Biomedicine (ITAB) (https://ieeexplore.ieee.org/document/5687751)

## How to run?

### Run on mini data as default option 
You just run <u>main.py<\u> in editor or enter <u>python main.py<\u> in command prompt.
(In <i>img<\i> directory, there are 2 images for the test. These images are part of mini-MIAS database. (http://peipa.essex.ac.uk/info/mias.html) ) 

### User mode
If you want to replace the mini data with your own data, put your images to img directory or edit path for your direrectory in <u>main.py<\u>.   
If you change parameters of your experiment, you can change parameters by changing the default value of the argument in <u>main.py<\u> or you can you the command line in command prompt.
- You can see all the adjustable parameters and usage. </pre> python main.py --help</pre>
(For example, if you want to cluster with 5 clusters, enter this command in your command prompt.  </u>python main.py -c 5<\u>)

## Results

<pre>
Getting filtered image..(This process can be time consuming.)
Time : 53.16970419883728
Iteration 0 : cost = 383.503160
Iteration 1 : cost = 130.096540
Iteration 2 : cost = 52.057745
Iteration 3 : cost = 36.463114
Iteration 4 : cost = 33.625992
Iteration 5 : cost = 40.136341
Iteration 6 : cost = 42.462534
Iteration 7 : cost = 29.869172
Iteration 8 : cost = 16.829851
Iteration 9 : cost = 10.073875
Iteration 10 : cost = 6.756716
Iteration 11 : cost = 4.957472
Iteration 12 : cost = 3.912657
Iteration 13 : cost = 3.158448
Iteration 14 : cost = 2.573333
Iteration 15 : cost = 2.098461
Iteration 16 : cost = 1.710719
Iteration 17 : cost = 1.394245
Iteration 18 : cost = 1.136231
Iteration 19 : cost = 0.925994
Iteration 20 : cost = 0.754842
Iteration 21 : cost = 0.615388
Iteration 22 : cost = 0.501762
Iteration 23 : cost = 0.409169
Iteration 24 : cost = 0.333715
Iteration 25 : cost = 0.272221
Iteration 26 : cost = 0.222079
Iteration 27 : cost = 0.181186
Iteration 28 : cost = 0.147834
Iteration 29 : cost = 0.120628
Iteration 30 : cost = 0.098434
Iteration 31 : cost = 0.080326
Iteration 32 : cost = 0.065552
Iteration 33 : cost = 0.053496
Iteration 34 : cost = 0.043659
</pre>

|Image| Result |
|:---:|:---: |
|mdb321.jpg|<img src = 'result.png'>|
|mdb322.jpg|<img src = 'result2.png'>|  


## Troubleshooting:
1. If it is not an 8-bit image, the code needs to be modified.
2. When there is a problem with the environment, you can try this command line in your command prompt. <pre> pip install -r requirements.txt </pre>

## References
* [1] [Z. Chen and R. Zwiggelaar "A Modified Fuzzy C Means Algorithm for Breast Tissue Density Segmentation in Mammograms." IEEE/Information Technology and Applications in Biomedicine (ITAB) 2010.](https://ieeexplore.ieee.org/document/5687751)
* [2] [J. Song and Z. Zhang "A Modified Robust FCM Model with Spatial Constraints for Brain MR Image Segmentation." Information 2019.](https://www.researchgate.net/publication/331278874_A_Modified_Robust_FCM_Model_with_Spatial_Constraints_for_Brain_MR_Image_Segmentation)
* https://github.com/ab93/SIFCM

## TODO:
- [ ] It takes a lot of time to get the filtered image. This problem can be solved by using numpy.lib.stride_tricks.as_strided.  
# PCA and Clustering
Here is some of my scientific stats (not published, otherwise see refs). Basically, here are steps of validation and analyses of a typical neural response.

## 1. Data representation
###  raw data - visualization of neural response from volume scanning
<img src="https://github.com/nan0445/Stats-Projects/blob/master/pic/PN_AL_volume_scanning.gif" width="30%" height="30%">   <img src="https://github.com/nan0445/Stats-Projects/blob/master/pic/PN_response.gif" width="29%" height="30%">

Firstly, stacks of images were 3D reconstructed for visualizing neural terminals and it's responses to stimuli.

<img src="https://github.com/nan0445/Stats-Projects/blob/master/pic/odor_response.png" width="50%" height="50%">

Secondly, neural activities were transfered as the ratio of changing activities over basal activities.(sample of three responses were shown above)

### PCA (Principal Component Analysis)
The above responses (could be hundreds or thousands) can be encoded by dozens and hundreds of "channels" of a neuron's terminal. Therefore, it is intuitive to apply PCA on the response representation space for data visualization. The methods we applied here are 'princomp' function in Matlab or 'PCA' function in Python Scikit-learn module

![](https://github.com/nan0445/Stats-Projects/blob/master/pic/PCA_PN_odor_responses.png)

1-D PCA reconstruction representation, subregion "channels" encoded.

![](https://github.com/nan0445/Stats-Projects/blob/master/pic/PN-PCA-LH1.png)

2-D PCA, whole region encoded

## 2. Clustering and Regression
The 1-D PCA or 2-D PCA generated a reduced representation space. We can then calculate the similarity or correlations within the data set by the reduced space. For 2-D pattern similarity comparisons, the image matrix was first flattened. The Euclidean and Cosine distances were then calculated as a parameter for clustering. (below shows a sample of similarity comparison and Euclidean distances for clustering)

![](https://github.com/nan0445/Stats-Projects/blob/master/pic/correlations.png)

This method can be further applied to other neural terminals, and if the same set of stimuli were presented, the correlations between different neural terminals can be calculated by regression. (below shows a linear correlation between A neuron and B neuron)

![](https://github.com/nan0445/Stats-Projects/blob/master/pic/regression.png)

(All of the analyses were performed in either Matlab or Python Scikit-learn tool)

# APTOS-2019-Blindness-Detection
Kaggle Competition...

### Description :
Millions of people suffer from diabetic retinopathy, the leading cause of blindness among working aged adults. Aravind Eye Hospital in India hopes to detect and prevent this disease among people living in rural areas where medical screening is difficult to conduct.<br>
I am going to build a machine learning model to speed up disease detection.I have to work with thousands of images collected in rural areas to help identify diabetic retinopathy automatically.

### Data Description :
Large set of retina images taken using fundus photography under a variety of imaging conditions.
A clinician has rated each image for the severity of diabetic retinopathy on a scale of 0 to 4:
+ 0 - No DR
+ 1 - Mild
+ 2 - Moderate
+ 3 - Severe
+ 4 - Proliferative DR

[Download the Dataset](https://www.kaggle.com/c/aptos2019-blindness-detection/data)

<details>
  <summary>Evaluation</summary>
Submissions are scored based on the quadratic weighted kappa, which measures the agreement between two ratings. This metric typically varies from 0 (random agreement between raters) to 1 (complete agreement between raters). In the event that there is less agreement between the raters than expected by chance, this metric may go below 0. The quadratic weighted kappa is calculated between the scores assigned by the human rater and the predicted scores.
<br><br>
Images have five possible ratings, 0,1,2,3,4.  Each image is characterized by a tuple (e,e), which corresponds to its scores by Rater A (human) and Rater B (predicted).  The quadratic weighted kappa is calculated as follows. First, an N x N histogram matrix O is constructed, such that O corresponds to the number of images that received a rating i by A and a rating j by B. An N-by-N matrix of weights, w, is calculated based on the difference between raters' scores:
<br><br>
An N-by-N histogram matrix of expected ratings, E, is calculated, assuming that there is no correlation between rating scores.  This is calculated as the outer product between each rater's histogram vector of ratings, normalized such that E and O have the same sum.
</details>

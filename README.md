# YOLOv8_DeepSORT_TRACKING

# `Introduction to DeepSORT`
  DeepSORT is a computer vision tracking algorithm for tracking objects while assigning an ID to each object. DeepSORT is an extension of the SORT (Simple Online  Realtime Tracking) algorithm. DeepSORT introduces deep learning into the SORT algorithm by adding an appearance descriptor to reduce identity switches, Hence making tracking more efficient. To understand DeepSORT, First Let’s see how the SORT algorithm works.`



# `DeepSORT Architecture.`

![archi](https://user-images.githubusercontent.com/98689629/212268087-c1cef949-3039-4038-bfce-c92fd195e3d6.jpg)




SORT performs very well in terms of tracking precision and accuracy. But SORT returns tracks with a high number of ID switches and fails in case of occlusion. This is because of the association matrix used. DeepSORT uses a better association metric that combines both motion and appearance descriptors. DeepSORT can be defined as the tracking algorithm which tracks objects not only based on the velocity and motion of the object but also the appearance of the object.

For the above purposes, a well-discriminating feature embedding is trained offline just before implementing tracking. The network is trained on a large-scale person re-identification dataset making it suitable for tracking context. To train the deep association metric model in the DeepSORT cosine metric learning approach is used. According to DeepSORT’s paper, “The cosine distance considers appearance information that is particularly useful to recover identities after long-term occlusions when motion is less discriminative.” That means cosine distance is a metric that helps the model recover identities in case of long-term occlusion and motion estimation also fails. Using these simple things can make the tracker even more powerful and accurate 



# Semantic_segmentation_thesis

Segmentation of cardiac muscle cells images
Automating data acquisition and processing is common practice in both microscopy
and computer vision fields. To classify and localize objects of interest (cardiomy-
ocytes in this case) in microscopy images, segmentation may be performed. In this
particular case, semantic segmentation by using deep neural networks was used as
the core mean to perform mentioned task and software providing possibility of pro-
cessing unlabeled data or training neural network architectures on labeled data was
implemented. This work does a brief introduction to optical microscopy, inspects
segmentation and deep learning in detail and finally describes the process from
preparing data, implementing and training neural networks, to design of the final
software.
----------------------------------------------------------------------------------
After research, neural networks implementation, training and evaluation, best models for given task were chosen and from further inspection SegNet and Xception Unet with residual blocks were chosen for the final algorithm
![Screenshot from 2022-04-01 11-36-40](https://user-images.githubusercontent.com/102659492/161237977-c919c786-f0b4-4981-80dc-607e36609e7e.png)

The final algorithm takes microscopy image(s), cuts them into smaller pieces for the machine to be able to process them. Then the cut tiles are segmented, joined back together which results in the segmentation map of the initial image. After that, segmap is binarized where objects of interests are 1s and the rest zeros, binary closing is performed and blobs above certain threshold are detected.
![Screenshot from 2022-04-01 11-37-26](https://user-images.githubusercontent.com/102659492/161238578-1e37729e-5633-4310-b0dd-0f88ae683778.png)
![Screenshot from 2022-04-01 11-37-34](https://user-images.githubusercontent.com/102659492/161238601-956e98e7-cf2e-4eab-acf5-fc6ce060e840.png)

The jupyter notebooks provide possibility to process new unlabeled data and to train neura network models on the labeled dataset

# Brain MRI Classification using Deep Learning | Pytorch
A Brain tumor is considered as one of the aggressive diseases, among children and adults. Brain tumors account for 85 to 90 percent of all primary Central Nervous System(CNS) tumors. Every year, around 11,700 people are diagnosed with a brain tumor. The 5-year survival rate for people with a cancerous brain or CNS tumor is approximately 34 percent for men and36 percent for women. Brain Tumors are classified as: Benign Tumor, Malignant Tumor, Pituitary Tumor, etc. Proper treatment, planning, and accurate diagnostics should be implemented to improve the life expectancy of the patients. The best technique to detect brain tumors is Magnetic Resonance Imaging (MRI). A huge amount of image data is generated through the scans. These images are examined by the radiologist. A manual examination can be error-prone due to the level of complexities involved in brain tumors and their properties. 
Credits : [Kaggle
](https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri)
## The Dataset Acquisition
The Data set is collected from one of the Kaggle competitions. Click [here](https://www.kaggle.com/sartajbhuvaji/brain-tumor-classification-mri) to download the data. 
 
 ## The Data Preparation
 For better results from the model certain changes are done to the dataset.


1.   All the images are resized to 512x512 since some of them differ in their size
2.   Padding of 8 pixels is added onto the sides of the image in the form of reflection of the image.
3. The image is then again cropped randomly to get 512x512 pixels.
4. The images are flipped along their horizontal axis.
5. The image pixels are converted to tensor
6. Normalize all values so that they lie in range -1 to 1 using means and standard deviations for every channel

## Defining the Model
This is done by using **Pytorch library** and along with this some helper methods are also defined which is in the notebook. A pretrained **ResNet18 model** is used to train our model. The  model is named MRIModel and it inherits from our previously created image classification base class. So this is using **Transfer Learning** Method for training the model. The Model uses GPU for training if available. 

Further steps are discussed in the jupyter notebook





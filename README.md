# A-CNN-model-image-classification
 A Convolutional Neural Networks on Dogs and Cats dataset (images) to classify them. 
Here we have 2 categories of animals (dogs vs cats). Each dataset has about 12500 images. For simplification (in Running) I just used 500 images from each category.
First I imported images and defined size (in pixels) to resize all the images into a unique size.
Then I converted them into NumPy arrays so I could feed them to the model.
After that, I shuffled the data because each category was in a separate folder so if we do not shuffle them all images from the first category will show up in a line and then the next one which can cause lots of issues for the model. 
I also split the dataset into X (inputs) and y (category) then reshaped X to make it an N by 1 array.
Then I saved the data as a pickle with makes it faster if you want to try other options with the model.
### Standardizing
As we are dealing with images, before using ML, we need a standard dataset, for this reason, I just applied X / 255 to all parts of the X because the maximum number is (always) 255 and by dividing them to 255 we can have numbers bin range [0,1]

After standardizing I imported necessary libraries then converted the input array to a Tensors.

### Model
In the end, I implemented Convolutional Neural Network as it is described in the model and plotted the training accuracy VS validation accuracy and training loss VS validation loss.

### Problem
The model seems great (91 % accuracy) but clearly, according to the plots we are having an issue which I believe is because of using a small training dataset instead of the whole dataset. 

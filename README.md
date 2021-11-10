# Classifying skin lesions with SNNs

This project evaluated the use of Siamese Neural Networks with triplet loss for
classifying skin disease images and identifying previously unseen classes. The data used for the project
can be downloaded from the following URLs:

ISIC2019: https://challenge.isic-archive.com/data
HAM10000: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T
PADS-UFES-20: https://data.mendeley.com/datasets/zr7vgbcyr2/1
LFW: http://vis-www.cs.umass.edu/lfw/#download 
(The specific subset of images downloaded from the above link is "Subset of images - George_W_Bush")

To use the provided code, the instructions are the same with minor exceptions for each file:

1) In google drive, upload each zipped datafile into a folder called "Data".

2) Open the code in google colaboratory.

3) Run the first two cells to install the correct versions of h5py and scikit-learn then restart the runtime.

4) Run each cell, including mounting the google drive to the notebook.

5) Run the desired downsampling and augmentation cell.

6) Run each cell, and select desired model for embedding layer by running the corresponding cell.

7) Run each cell until the text box "Define name of model or load previous".

8) The loss function, optimizer and other hyperparameters such as batch size and embedding length
   can be specified here. For batch all triplet selection, specify "keras_batch_all_triplet_loss" 
   and for batch hard use "keras_batch_hard_triplet_loss"

7) Choose the name of the model with the "name" variable. Enter a previous model's name here to load it.

8) Run this cell, and in next specify same loss and optimizer. Running this cell initiates model training. If 
   loading a previous model running this cell is not necessary.

9) Run the next cell to load model with lowest validation loss.

10) Run reminaing cells to obtain the metrics that they are labelled with.

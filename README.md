# satellite-to-google-map
This is a Pix2pix model for translating satellite images to google map images.
Intial dataset had train and val folders in which 1097 and 1099 images were there respectively.
Images were of size 600*1200 where half image was satellite and another half was google map image.
I had separated the images,  600*600 size satellite images in xtrain,xval and 600*600 size google map images in ytrain,yval.
After removing some corrupted images xtrain and ytrain comprise of 999 images.
Images are then resized to 256*256 and normalized from (0-255) to(-1,1) , then stored in the form of compressed numpy array where 2 lists are xtrain and ytrain respectively . Filename="maps_256.npz".

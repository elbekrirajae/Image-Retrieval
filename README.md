# Image-Retrieval


The Holidays dataset is a public 1 set of images which mainly contains some personal holidays photos. The dataset contains
1491 images in total : 500 queries and 991 corresponding relevant images.

### Computing image descriptors: 
Using image pixels directly as features is the simplest idea to compute the similarity between
two images. We will use a distance between the raw pixels between the two images. Resize the images to 16x16x3 and flatten
the pixels as a vector.
We compute a similarity score with the euclidean distance with all remaining images and then calculate the precision and recall.

Furthermmore, implement other descriptors than just the raw pixels : gray level vs color histogram, Haralick parameters of GLCM vs
Local Binary Patterns (LBP), HOG descriptors, etc... and see how performance improves

## Bag of Visual Words : Implement a simple version of the Bag of Visual Words model :
— divide images into patches
— compute a dictionary of visual words (VW) with k-means
— assign each patch to its closest VW
— describe each image with a histogram of the assigned VW

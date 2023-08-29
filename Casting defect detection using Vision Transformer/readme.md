# Objective:
The objective of this project is to use a dataset of a casting defects availble on kaggle to classify the images into defective or non-defective part.
# Model used:
I created my own Vision Transfomer model from scratch as explained in the paper " AN image is worth 16X16 words" 
https://doi.org/10.48550/arXiv.2010.11929. 
I also used transfer learning and fine tuning a hugging face vision transformer to train on the dataset used in this project.
# Vision Transformer Model:
The Vision Transformer, or ViT, is a model for image classification that employs a Transformer-like architecture over patches of the image. An image is split into fixed-size patches, each of them are then linearly embedded, position embeddings are added, and the resulting sequence of vectors is fed to a standard Transformer encoder. While CNN uses convolution that is a local operation bounded to a small neighborhod of an image ViT uses self-attention a global operation that draws information from the whole image. This results into better performance in certain tasks. The ViT requires a large dataset to perform well, hence if a smaller dataset is available it is better to use CNN or use transfer learning and fine tuning on a ViT pretrained on a larger dataset.


![](ViT.png) 


# Result:
As the available dataset was really small, it was obvious that the performance of the ViT trained on this dataset wouldn't be good. But finetuning a hugging face ViT yielded into an accuracy of around 95%.

# ISL_RSA_DigitObject_Visual

## Sample data:
- Please download the sample data from this link:
(Here, we provide sample data due to the IRB. However, we have a plan to release data public in the future.)
1. 'vgg16_weights.txt' [1-2]
2. 'Train_Val.npz' [3-4]
3. 'Sample_fMRI_data.npz'
- Please download the trained model (for the visualzation) in this link:
1. 'net-55.ckpt.data-00000-of-00001', 'net-55.ckpt.index', 'net-55.ckpt.meta'

### Data structure: 
The input ‘.npz’ file includes:
- ‘imgnet_tr_X’, ‘imgnet_val_X’ are training and validation set of six object categories from ImageNet
- ‘mnst_tr_X’, ‘mnst_val_X’ are training and validation set of ten digit categories from MNIST
- ‘imgnet_tr_y’, ‘imgnet_val_y’, 'mnst_tr_y', 'mnst_val_y' are the labels for the training and validation
- Training set contains 10 sample images for each category.
- Validation set contains 10 sample images for each category.

## Running code:
- Run the code in order.
- Follow the comments in the notebook.

## References:
* [1] Simonyan, K., & Zisserman, A. (2014). Very deep convolutional networks for large-scale image recognition. arXiv preprint arXiv:1409.1556.
* [2] https://keras.io/api/applications/vgg/
* [3] LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. (1998). Gradient-based learning applied to document recognition. Proceedings of the IEEE, 86(11), 2278-2324.
* [4] Deng, J., Dong, W., Socher, R., Li, L. J., Li, K., & Fei-Fei, L. (2009, June). Imagenet: A large-scale hierarchical image database. In 2009 IEEE conference on computer vision and pattern recognition (pp. 248-255). Ieee.

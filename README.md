# ISL_RSA_DigitObject_Visual
* These are the Python codes for our representationsl similarity analysis (RSA) for handwritten digits and naturalistic objects between human and CNN.

## Sample data:
Please download the sample data from this link:
- [Sample_Data.zip](http://bspl.korea.ac.kr/Research_data/digitobject/Sample_data.zip)
  - Here, we provide sample data. However, we plan to release the data in the future.

The ‘Sample_Data.zip’ file includes:
- vgg16_weights.txt 
  - Pretrained weights of VGG-16 [1] for ImageNet 1000 class classification provided by Keras [2]
- Train_Data.npz / Val_Data.npz 
  - 10 sample images per category [3, 4] for training/validation of the CNN.
- Sample_fMRI_data.npz
  - GLM beta-valued map per category from a participant.
- net-55.ckpt.data-00000-of-00001 / net-55.ckpt.index / net-55.ckpt.meta
  - Trained CNN model.

## Running code:
- Run the code in order following the comments in the notebook.

  - 01_Training and validation of the CNN model for digit and object recognition.ipynb
    - Training and validation of the CNN model for digit and object recognition using sample data.
    
  - 02-1_Activation Maximization.ipynb
    - Trained CNN model visualization using activation maximization method [5].
    
  - 02-2_t-SNE of CNN.ipynb
    - t-SNE embeddings [6] of trained CNN model visualization using sample data.
    
 ![Github_t-SNE](https://user-images.githubusercontent.com/39120886/129598375-248e10fe-54ee-48cb-9597-130b6536eaf7.png)

  - 03_MVPA_Neural_RDMs.ipynb
    - Obtain searchlight neural RDM using sample data.
    
  - 04_RSA_From_CNN_Perspective.ipynb
    - Apply PCA to CNN features for sample data.
    - Obtain CNN layer RDM.
    - RSA between neural RDM obtained from '03_MVPA_Neural_RDMs.ipynb' and CNN layer RDM.
    - Maximally similar layer assignment.

  - 05_RSA_From_Human_Perspective.ipynb
    - Create human categorical perception codes.
    - RSA between neural RDM obtained from '03_MVPA_Neural_RDMs.ipynb' and hypothetical codes.
    
  - 06-1_Cosine_CNN_Code.ipynb
    - Cosine similarity between CNN layer RDM and human categorical perception codes.
    
  - 06-2_RSA_CNN_Code_Neural.ipynb
    - RSA between CNN layer RDM and neural RDM in ROIs found from human categorical perception codes.
    
## References:
* [1] Simonyan, K., & Zisserman, A. (2014). Very deep convolutional networks for large-scale image recognition. arXiv preprint arXiv:1409.1556.
* [2] https://keras.io/api/applications/vgg/
* [3] LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. (1998). Gradient-based learning applied to document recognition. Proceedings of the IEEE, 86(11), 2278-2324.
* [4] Deng, J., Dong, W., Socher, R., Li, L. J., Li, K., & Fei-Fei, L. (2009, June). Imagenet: A large-scale hierarchical image database. In 2009 IEEE conference on computer vision and pattern recognition (pp. 248-255). Ieee.
* [5] Erhan, D., Bengio, Y., Courville, A., & Vincent, P. (2009). Visualizing higher-layer features of a deep network. University of Montreal, 1341(3), 1.
* [6] Van der Maaten, L., & Hinton, G. (2008). Visualizing data using t-SNE. Journal of machine learning research, 9(11).

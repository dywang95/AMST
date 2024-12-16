# AMST
Aluminum profile surface defects (APSDs) significantly impact product performance and safety, necessitating efficient and accurate inspection methods. Traditional high-resolution imaging and deep learning models are resource-intensive, posing challenges for portable devices. This paper proposes an Adaptive Mask Swin Transformer (AMST) for efficient super-resolution (SR) of APSD images. AMST introduces an adaptive mask module (AMM) to selectively process high-frequency defect regions, enhancing feature extraction while reducing computational cost. An efficient feature enhancement module (EFEM) further improves performance by integrating non-local and local information. Extensive experiments on the newly introduced APSDs-SR dataset demonstrate that AMST achieves state-of-the-art SR performance with reduced parameters and floating-point operations. Additionally, AMST’s SR results facilitate downstream tasks such as defect classification and detection.

Dependencies
--
* python >= 3.6.0
* pytorch >= 1.7.0
* torchvision >= 0.8.0

Dataset
--
Download Training Set and Testing Set ([APSDs](https://drive.google.com/drive/folders/19OSjKiOZmzu8T_yhehrQS2vrV_k8ncH8?usp=sharing))    

Training
--   
1. Revise the ``dataroot_H`` and ``dataroot_L`` in ``options/train_sr_lightweight.json``  
2. Run ``main_train.py``  

Testing
--
1. Revise the ``model_path``, ``folder_lq`` and ``folder_gt`` in ``main_test.py``  
2. Run ``main_test.py``

[AMST test results](https://drive.google.com/drive/folders/19OSjKiOZmzu8T_yhehrQS2vrV_k8ncH8?usp=sharing)

Acknowledgement
--
We borrow some codes from [KAIR](https://github.com/cszn/KAIR) and [SwinIR](https://github.com/JingyunLiang/SwinIR). We thank the authors for their great work.

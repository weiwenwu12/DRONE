# DRONE
DRONE focuses on reconstructing  good images from CT scanner with 60 views of fan-beam geometry. 
# DRONE: Dual-domain Residual-based Optimization Network for Sparse-view CT Reconstruction

Before using this code, you need to install Python and the TensorFlow library. The code, trained models and test datasets can be downloaded from Zenode (https://zenodo.org/record/4724096) 

If you use the code, please cite our work
@article{
	title={ DRONE: Dual-domain Residual-based Optimization Network for Sparse-view CT Reconstruction },
	author={Wu, Weiwen; Hu, Dianlin; Yu, Hengyong; Niu,Chuang; Vardhanabhuti, Varut and Wang, Ge},
	year={2021}; Publisher: {IEEE Transaction on Medical Imaging}
}

If you have any question about the code, please contact with the author, email: weiwenwu12@gmail.com.

## Environment:
Windows 10:
python 3.6.5, cuda 10.0, tensorflow 1.13.1 

Because odl reconstruction toolbox (https://github.com/odlgroup/odl/tree/master/odl/tomo) is used in DRONE, you need to install the odl software using easy-install strategy.

More details about implementation:
There are five folders under the root path, i.e.,Data_Generate, Dataset, Embedding-module, Refinement-module and Awareness-module

Dataset: the path used to save original datasets, including the training datasets and testing datasets;

Data_Generate: generating the initial projection, i.e., load original images of 20 patients to generate the projection data of 60 views;

Embedding-module: the data generation files to generate the training projections and images;  the training files used to train the projection and image domain networks, the test files employed to generate the training datasets for next module;

Refinement-module: the data generation files to generate the training projections and images; the training files used to train the residual refinement projection and image domain networks, the test files employed to generate the network reconstruction results;

Awareness-module: It can generate the final reconstruction results. This zip file (under the Embedding and Refinement modules) contains the four trained networks provided by authors. The CASES 1-4 results in DRONE paper can be reproduced by running the test-DRONE.py with modifying the path under the CNNhelper.py. The detailed ablation study results can be reproduced by implementing Ablation-Study from CASE 5. 

If you would like to test more datasets, please contact with one of authors in the referred paper. If you want to train the networks by yourself, please first download the datasets from the publically website: https://public.cancerimagingarchive.net/nbia-search/. Furthermore, if you want to retrain the experiment networks, please send the email to one of coauthors to ask for datasets.

# ProteinNet
Deep learning based protein characterization from 3D point clouds.

This project has been developed in the frame of the SHREC 2021 contest http://shrec2021.drugdesign.fr/. It consists of proposing approaches for indexing proteins from 3d shapes in the form of point cloud and associated metadata. The developed approach exploits deep learning techniques to characterize protein shape. In particular, the approach includes a data normalization module by realigning the 3D coordinates of the proteins towards optimizing indexing performances. 

![proteinnet](https://user-images.githubusercontent.com/86927146/161537902-289fe596-29c7-4c22-be8e-3c93a9ae0d4e.png) *Fig. 1 ProteinNet deep architecture for protein point cloud transformation into canonical representation. Step (1): affine transformation matrix estimation. Step (2): protein point cloud transformation using the estimated affine matrix. Step (3): similarity calculation between the original protein point cloud (the input) and its transformed point cloud. Step (4): cosine similarity loss calculation between the original input protein point cloud and its transformation; and back–propagation over the network to optimize the estimation of the affine transformation matrix. (first published in [1]).*

# How to use the code?
**Steps:**
> * Download the dataset (queries_ply_shape.tar.gz + ply_shape.tar.gz) from the contest website and unzip it.
> * Run the "Preprocess.ipynb" file to normalize data and simplify the protein shapes.
> * Run the "ProteinNetModel.ipynb" file to characterize proteins and produce the dissimilarity matrix.

**Note:**
> * Code can be run cell by cell using Google Colab plateform for example. 
> * External codes that have been used in this project are referenced by a comment in the head of concerned cells.


# Team
**Project leaders:**

> * Halim Benhabiles, JUNIA, IEMN CNRS Lille, halim.benhabiles@junia.com
> * Karim Hammoudi, Université de Haute-Alsace, IRIMAS, karim.hammoudi@uha.fr

Note: code has been developed by Halim Benhabiles.

**Contributors:**

> * Adnane Cabani, ESIGELEC/IRSEEM, adnane.cabani@esigelec.fr
> * Feryal Windal, JUNIA, IEMN CNRS Lille, feryal.windal@junia.com
> * Mahmoud Melkemi, Université de Haute-Alsace, IRIMAS, mahmoud.melkemi@uha.fr

# How to cite this work?

[1] Langenfeld, F., Aderinwale, T., Christoffer, C., Shin, W. H., Terashi, G., Wang, X., Kihara, D., Benhabiles, H. et al. Surface-based protein domains retrieval methods from a SHREC2021 challenge. Journal of Molecular Graphics and Modelling, Elsevier (2022). https://doi.org/10.1016/j.jmgm.2021.108103

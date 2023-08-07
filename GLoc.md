### Global Localization in Large-scale Point Clouds via Roll-pitch-yaw Invariant Place Recognition and Low-overlap Global Registration

Zhong Wang<sup>1</sup>, Lin Zhang<sup>1</sup>, Shengjie Zhao<sup>1</sup>, and Yicong Zhou<sup>2</sup>

<sup>1</sup>School of Software Engineering, Tongji University, Shanghai, China

<sup>2</sup>Department of Computer and Information Science, University of Macau, China

---

#### Introduction

>  This is the website for our paper "Global Localization in Large-scale Point Clouds via Roll-pitch-yaw Invariant Place Recognition and Low-overlap Global Registration".

![Framework](framework.png)

<center style="color:#C0C0C0;text-decoration:underline">Figure 1. Overview of our framework. In the offline RpyPR training phase, sampled query-positive-negative tuples are aligned to the ground to derive projection parameters. With these parameters, 2D occupation grids are projected from the 3D occupancy voxels. Such 2D grids are subsequently fed into a deep encoder and NetVLAD layers to aggregate place embeddings, which are used to update the search tree and network under the supervision of the triplet loss. During online global localization (RpyPR recognition and LoPcGR registration), the query obtains its place embedding and employs it to retrieve the response and the corresponding occupancy grids from the gallery. At last, by estimating the transformation between the 2D grids and combining the projection parameters, the full 6-DoF pose can be determined.</center>

---

#### Additional Evaluations on Generalization Ability

To further illustrate the strong generalization ability of our proposed RpyPR, we use the model trained on the KITTI dataset to make a test on the NuScenes dataset for autonomous driving. The obtained results are shown in Table 1. As can be seen, the proposed RpyPR shows good generalization on new data sequences, while other similar learning-based schemes only GeoTransformer [3] performs moderately well, with unsatisfactory results for both PointNetVLAD [1] and LPD-Net [2].

<center style="color:#C0C0C0;text-decoration:underline">Table 1. Generalization ability comparison. The recall rates below of NuScenes are produced by the models trained on KITTI.</center>

|                    |   Top-1    |   Top-5    |   Top-10   |   Top-20   |
| :----------------: | :--------: | :--------: | :--------: | :--------: |
|  PoinNetVLAD [1]   |   0.2293   |   0.3997   |   0.4867   |   0.5654   |
|    LPD-Net [2]     |   0.4654   |   0.6790   |   0.7591   |   0.8357   |
| GeoTransformer [3] |   0.6934   |   0.8268   |   0.8843   |   0.9185   |
|  **RpyPR (ours)**  | **0.9692** | **0.9911** | **0.9945** | **0.9966** |



---

#### Source Codes

[GLoc Codes](scan-to-scan.zip)

#### References

[1] M. A. Uy and G. H. Lee, "PointnetVLAD: Deep point cloud based retrieval for large-scale place recognition," in Proc. IEEE Conf. Comput. Vis. Patt. Recog., Salt Lake City, USA, Jun. 2018, pp. 4470–4479.

[2] Z. Liu, S. Zhou, C. Suo, P. Yin, W. Chen, H. Wang, H. Li, and Y. H. Liu, "LPD-Net: 3D point cloud learning for large-scale place recognition and environment analysis," in Proc. IEEE/CVF Int. Conf. Comput. Vis., Seoul, Korea, Oct. 2019, pp. 2831–2840.

[3] J. Ma, J. Zhang, J. Xu, R. Ai, W. Gu, and X. Chen, "OverlapTransformer: An efficient and yaw-angle-invariant transformer network for LiDAR-based place recognition," IEEE Robot. Autom. Letters, vol. 7, no. 3, pp. 6958–6965, 2022.

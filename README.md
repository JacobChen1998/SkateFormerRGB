# SkateFormerRGB

Action recognition has always been a highly challenging task. Today’s advanced technologies include RGB-based and skeleton-based action recognition. Skeleton-based action recognition can achieve real-time, multi-person action recognition, but it lacks the ability to reference interactions between people and objects. While RGB-based full-image action detection is accurate, it is nearly impossible to achieve real-time, multi-person action recognition. Based on these characteristics, we have referenced the SkateFormer architecture, integrating person-region images for training, and achieved state-of-the-art results.

In this repository, we implement the integration of RGB information into SkateFormer for multi-person action recognition. Our contributions are as follows:

1. Modified the original 25 keypoints to 17 keypoints (COCO format).
2. Added an RGB feature extractor to the network architecture and performed fusion with skeleton information.
3. Described the process for using YOLOv8-Pose to collect skeleton/RGB data.
4. Compared the performance of the modified model with the original SkateFormer.

## <div align="center">Network structure</div>

<div align="center">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_network_structure.png" width="70%" /></a>
</div>

## <div align="center">Data flow for preprocessing and training</div>

<div align="center">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_dataPreprocess_training.png" width="70%" /></a>
    <p>Figure : Network Sturcture of SkateFormerRGB (we using value generated on SkateFormer origin eval function )</p>
</div>

## <div align="center">Result</div>

<div align="center">
<p>Table : Skeleton Based Action Recognition on NTU RGB+D 120 </p>
    
| Model                                    | Validation Accuracy (%)                             | Parameters (M)          |
| ---------------------------------------- | --------------------------------------------------- | ------------------------ |
| <center>DeGCN                            </center> | <center>[91.0](https://paperswithcode.com/sota/skeleton-based-action-recognition-on-ntu-rgbd-1)</center> | <center>-   </center>       |
| <center>STGCN (PYSKL)                    </center> | <center>[84.7](https://paperswithcode.com/sota/skeleton-based-action-recognition-on-ntu-rgbd-1)</center> | <center>1.41</center>       |
| <center>SkateFormer 25 keypoints         </center> | <center>[89.8](https://paperswithcode.com/sota/skeleton-based-action-recognition-on-ntu-rgbd-1)</center> | <center>2.02</center>    |
| <center>SkateFormerRGB 17 keypoints (our)</center> | <center>95.8</center>                                                                                    | <center>3.75</center>       |

</div>

<div align="center">
  <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/BestValidationResult.png" width="50%" /></a>
  <p>Figure : Validation Accuracy that model trained with 90 epochs (we using value generated on SkateFormer origin eval function )</p>
</div>


### Acknowledgement
This repository is built upon [SkateFormer](https://github.com/KAIST-VICLab/SkateFormer).

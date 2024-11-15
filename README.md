# SkateFormerRGB

In this repository, we implement the integration of RGB information into SkateFormer for multi-person action recognition. Our contributions are as follows:

1. Modified the original 25 keypoints to 17 keypoints (COCO format).
2. Added an RGB feature extractor to the network architecture and performed fusion with skeleton information.
3. Described the process for using YOLOv8-Pose to collect skeleton/RGB data.
4. Compared the performance of the modified model with the original SkateFormer.

## <div align="center">Data flow for preprocessing and training</div>
<div align="center">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_network_structure.png" width="70%" /></a>
</div>

## <div align="center">Network Sturcture</div>
<div align="center">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_dataPreprocess_training.png" width="70%" /></a>
</div>

## <div align="center">Result Comprison</div>
<div align="center">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/model%20compare%20workflow.png" width="70%" /></a>
</div>

## <div align="center">Result (Skeleton Based Action Recognition on NTU RGB+D 120)</div>

<div align="center">
    
| Model                                    | Validation Accuracy (%)                             | Parameters (M)          |
| ---------------------------------------- | --------------------------------------------------- | ------------------------ |
| <center>STGCN (PYSKL)                    </center> | <center>[84.7](https://paperswithcode.com/sota/skeleton-based-action-recognition-on-ntu-rgbd-1)</center> | <center>1.41</center>       |
| <center>SkateFormer 25 keypoints         </center> | <center>[89.8](https://paperswithcode.com/sota/skeleton-based-action-recognition-on-ntu-rgbd-1)</center> | <center>2.02</center>    |
| <center>SkateFormerRGB 17 keypoints (our)</center> | <center>93.2</center>                                                                                    | <center>3.75</center>       |

</div>

<div align="center">
  <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/Compare_ConfidenceThreshold_and_Accuracy.png" width="50%" /></a>
</div>


### Acknowledgement
This repository is built upon [SkateFormer](https://github.com/KAIST-VICLab/SkateFormer).

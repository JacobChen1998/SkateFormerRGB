# SkateFormerRGB

In this repository, we implement the integration of RGB information into SkateFormer for multi-person action recognition. Our contributions are as follows:

Modified the original 25 keypoints to 17 keypoints (COCO format).
Added an RGB feature extractor to the network architecture and performed fusion with skeleton information.
Described the process for using YOLOv8-Pose to collect skeleton/RGB data.
Compared the performance of the modified model with the original SkateFormer.

## <div align="center">Data flow for preprocessing and training</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_network_structure.png" width="100%" /></a>
</div>

## <div align="center">etwork Sturcture</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_dataPreprocess_training.png" width="100%" /></a>
</div>

## <div align="center">Result Comprison</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/model_compare_workflow.png" width="100%" /></a>
</div>

### Installation
```bash
git clone https://github.com/JacobChen1998/SkateFormerRGB.git
[TODO]
```

# SkateFormerRGB

In this repository, we implement the integration of RGB information into SkateFormer for multi-person action recognition. Our contributions are as follows:

1. Modified the original 25 keypoints to 17 keypoints (COCO format).
2. Added an RGB feature extractor to the network architecture and performed fusion with skeleton information.
3. Described the process for using YOLOv8-Pose to collect skeleton/RGB data.
4. Compared the performance of the modified model with the original SkateFormer.

## <div align="center">Data flow for preprocessing and training</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_network_structure.png" width="70%" /></a>
</div>

## <div align="center">Network Sturcture</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/SkateFormerRGB_dataPreprocess_training.png" width="70%" /></a>
</div>

## <div align="center">Result Comprison</div>
<div align="center">
  <a href="https://roboflow.com/?ref=ultralytics">
    <img src="https://github.com/JacobChen1998/SkateFormerRGB/blob/main/figures/model%20compare%20workflow.png" width="70%" /></a>
</div>

### Result

| Model | Training Accuracy | Validation Accuracy | arameters | 
| ----------------------------------- | ---- | ---- |--- |
| SkateFormer 25 keypoints            | -    |  -  |  -  |
| SkateFormer 17 keypoints  (our)     | -    |  -  |  -  |
| SkateFormerRGB 17 keypoints (our)   | -    |  -  |  -  |

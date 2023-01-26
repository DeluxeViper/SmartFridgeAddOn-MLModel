# SmartFridgeAddOn-MLModel
An object detection model using Yolov7 for detecting ingredients

### Tools utilized:
- Roboflow
- Google Colab
- Python
- Pytorch
- Yolov7

### Datasets

Where all my datasets are: https://app.roboflow.com/deluxeviper

**Specific dataset urls:**

Apple (1803 images): https://app.roboflow.com/deluxeviper/fridge-ingredients-apple/overview

Orange (1599 images, trained for 55 epochs using Yolov7, produced 98% mAP@0.5, 96% P, 97% R): https://app.roboflow.com/deluxeviper/orange-fridge-ingredients/overview

###### Note for training bugs:
- If you run into the `RuntimeError: indices should be either on cpu or on the same device as the indexed tensor (cpu)` bug, then you must change the `yolov7/utils/loss.py` line 742 from `matching_matrix = torch.zeros_like(cost)` to `matching_matrix = torch.zeros_like(cost, device="cpu")`

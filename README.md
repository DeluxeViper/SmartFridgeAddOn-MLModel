# SmartFridgeAddOn-MLModel
An object detection model using Yolov7 for detecting ingredients

Tools utilized:
- Roboflow
- Google Colab
- Python
- Pytorch
- Yolov7

Dataset: https://app.roboflow.com/deluxeviper/fridge-ingredients/overview

Note for training bugs:
- If you run into the `RuntimeError: indices should be either on cpu or on the same device as the indexed tensor (cpu)` bug, then you must change the `yolov7/utils/loss.py` line 742 from `matching_matrix = torch.zeros_like(cost)` to `matching_matrix = torch.zeros_like(cost, device="cpu")`

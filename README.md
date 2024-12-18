# Road-Sign-Detection-using-YOLOv8
This project demonstrates the implementation of YOLOv8 for detecting and localizing road signs in images. The model is trained on a custom dataset and evaluated using metrics IoU. 
### Overview
This project involves:
1. Training the YOLOv8 model on a custom road sign dataset.
2. Visualizing predictions on train, validation, and test images.
3. Evaluating model performance using metrics like IoU.
### Features
1. State-of-the-Art Model: Utilizes the YOLOv8n pretrained model for transfer learning.
2. Custom Dataset: Processes and trains on road sign detection images.
3. Metrics Calculation: Computes Intersection over Union (IoU) for predicted and ground-truth bounding boxes.
4. Visual Results: Saves predictions with annotated bounding boxes for visualization.
### Model Training
The model is trained using YOLOv8n.pt (a lightweight pretrained YOLO model) for 30 epochs with optimized hyperparameters:
`
model.train(data='/content/Road_Sign_Detection/data.yaml', epochs=30, batch=-1, optimizer='auto', amp=True)
`
### Evaluation
The project computes IoU to evaluate predictions against ground-truth labels:
1. IoU Calculation: Measures the overlap between predicted and ground-truth bounding boxes.
2. Custom Script: Reads YOLO-format annotations and calculates the IoU.

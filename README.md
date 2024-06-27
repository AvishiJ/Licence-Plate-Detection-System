# Licence Plate Detection and Recognition using YOLO-V8 EasyOCR 🚀 

# About
This project integrates EasyOCR with Ultralytics YOLO for object detection and text recognition within detected objects.

![Screenshot 2024-06-27 222304](https://github.com/AvishiJ/Licence-Plate-Detection-System/assets/93474251/cd0801e5-ddab-4f2f-8c0f-754ec060e517)

## Requirements

- Python 3.x
- PyTorch
- OpenCV
- EasyOCR
- Hydra
- Ultralytics YOLO
  
 **Install Dependencies**:
    ```bash
    pip install torch torchvision torchaudio
    pip install opencv-python-headless
    pip install easyocr
    pip install hydra-core
    pip install ultralytics
    ```

## Usage

### Steps Performed in the Code

1. **Import Necessary Libraries**:
    - Imports Hydra, PyTorch, EasyOCR, OpenCV, and Ultralytics YOLO libraries and modules.

2. **Define the OCR Function**:
    - Extracts the region of interest from the image.
    - Converts the image to grayscale.
    - Uses EasyOCR to read text from the grayscale image.
    - Processes OCR results to extract and return the detected text.

3. **Create a Custom Detection Predictor Class**:
    - Inherits from `BasePredictor` to customize prediction behavior.

4. **Define Annotator Method**:
    - Returns an `Annotator` instance for annotating images with bounding boxes and labels.

5. **Define Preprocessing Method**:
    - Converts the input image to a PyTorch tensor and normalizes it.

6. **Define Postprocessing Method**:
    - Applies non-maximum suppression to filter out overlapping boxes.
    - Scales bounding boxes to the original image size.

7. **Define Write Results Method**:
    - Handles logging and saving of detection results.
    - Annotates the image with bounding boxes, labels, and OCR results.
    - Saves the annotated image and detection labels to files.

8. **Define Main Prediction Function**:
    - Uses Hydra to manage configuration.
    - Sets up model and image source.
    - Creates an instance of the custom `DetectionPredictor`.
    - Runs the predictor.

9. **Initialize EasyOCR Reader and Run Prediction**:
    - Initializes the EasyOCR reader with English language support.
    - Calls the `predict` function to start the prediction process.

This script will process the images, perform object detection and OCR, annotate the images, and save the results.

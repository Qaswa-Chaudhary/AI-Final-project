# License Plate Recognition System (LPR)

## **Overview**
The License Plate Recognition (LPR) System is a real-time computer vision project designed to detect and recognize vehicle license plates in video streams. The system utilizes machine learning and deep learning models to detect vehicles, track their movement, and extract license plate information for further processing.

## **Features**
- **Vehicle Detection & Tracking**:
  - Detects vehicles such as cars, bikes, buses, and trucks using YOLOv8.
  - Tracks vehicles across multiple video frames using the SORT algorithm.
- **License Plate Detection & Recognition**:
  - Detects license plates using a YOLO-based model.
  - Reads license plate text using EasyOCR.
- **Data Interpolation**:
  - Handles missing tracking data by interpolating bounding box positions across frames.
- **Visualization**:
  - Outputs processed videos with bounding boxes and license plate details overlaid.
- **CSV Export**:
  - Stores results in a CSV file containing details such as frame numbers, vehicle IDs, bounding boxes, license plate numbers, and confidence scores.

---

## **Technologies Used**

### **Programming Language**
- Python 3.12

### **Libraries & Frameworks**
- **OpenCV**: Video processing, image manipulation, and drawing bounding boxes.
- **YOLO (You Only Look Once)**:
  - YOLOv8n for vehicle detection.
  - YOLO-based model fine-tuned for license plate detection.
- **NumPy**: Array operations and bounding box handling.
- **Pandas**: Data management and CSV handling.
- **Scipy**: Interpolation of missing bounding box data.
- **SORT**: Simple Online and Realtime Tracking for vehicle and license plate association.
- **EasyOCR**: Optical Character Recognition for extracting text from license plates.

---

## **Project Structure**
- **`main.py`**: Main script for vehicle and license plate detection and tracking.
- **`util.py`**: Utility functions for license plate recognition and processing.
- **`add_missing_data.py`**: Script for interpolating missing tracking data.
- **`visualize.py`**: Script for drawing bounding boxes and visualizing results on video frames.

---

## **Workflow**
1. **Detection**:
   - YOLO detects vehicles and license plates in video frames.
2. **Tracking**:
   - SORT algorithm tracks vehicles and links them with detected license plates.
3. **OCR**:
   - EasyOCR extracts license plate text from cropped license plate images.
4. **Data Handling**:
   - Interpolation fills in missing data for skipped or occluded frames.
5. **Output**:
   - Results are exported as a CSV file.
   - A processed video with annotated results is saved for visualization.

---

## **Output**
- **CSV File**:
  - Contains details like frame numbers, vehicle IDs, bounding boxes, license plate text, and detection confidence scores.
- **Processed Video**:
  - Annotated with bounding boxes for vehicles and license plates, along with license plate text.

---

## **Conclusion**
The LPR System is a robust solution for real-time vehicle and license plate recognition. By integrating YOLO-based detection, SORT tracking, and OCR, it ensures accurate identification and tracking. Missing data is handled with interpolation, and results are effectively visualized and stored for further analysis.

# pYOLO
A MOOS robot middleware application integrating the YOLO object recognition library. Run on the SeaRobotics Surveyor autonomous surface vehicles.

## Usage
1. Place your custom model in: `pYOLO\yolo\custom_models`
2. Modify `input_source`, `weights`, and `python` in `pYOLO\YOLO.cpp` to reflect your web stream input source, your custom model, and the location of your python executable.

### Publishes
- DETECTED 
  - A boolean value indicates whether a object is detected (true) or not (false).
- CONF:
  - The confidence level of the object detection
- CLASS_LABEL
  - The label of the detected class in the image
- BOX_X
  - The x-coordinate of the bottom middle of the bounding box in the image where an object is detected.
- BOX_Y
  - The y-coordinate of the bottom middle of the bounding box in the image where a object is detected.

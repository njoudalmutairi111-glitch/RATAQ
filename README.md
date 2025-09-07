# RATAQ: Road Infrastructure Damage Detection

RATAQ is a deep learning project trained to detect common road infrastructure problems such as:
- Damaged sidewalks
- Cracks
- Potholes

This repository provides a trained model and a Jupyter Notebook (`rataq.ipynb`) for running inference and experimentation.

---

## Installation

The notebook is designed to run on **Google Colab**.  
Before starting, install the required dependencies:

```bash
!pip install ultralytics==8.0.20
!pip install roboflow
!pip install opencv-python
```

---

## Usage

This project is designed to run on **Google Colab**.  
To use the trained model:

1. Open the notebook `rataq.ipynb` in Google Colab.
2. Install dependencies by running:

```python
!pip install ultralytics==8.0.20
!pip install roboflow
!pip install opencv-python
```

3. Import required libraries:

```python
import os
from ultralytics import YOLO
import cv2
from google.colab.patches import cv2_imshow
import glob
```

4. Load the trained model and run inference:

```python
model = YOLO("best.pt")  # Replace with your model path
results = model("test_image.jpg")  # Replace with your input image
results.show()  # Display results
```

5. Replace `"test_image.jpg"` with your own images to detect road damages like cracks, potholes, or damaged sidewalks.

---

## Citation

If you use this project in your research, please cite:

```bibtex
@software{RATAQ,
  author = {Njoud Almutairi},
  title = {RATAQ: Road Infrastructure Damage Detection Model},
  url = {https://github.com/njoudalmutairi111-glitch/RATAQ},
  version = {1.0.0},
  year = {2025}
}
```

---

## License

This project is licensed under the [AGPL-3.0 License](LICENSE).  
It includes code from [Ultralytics YOLO](https://github.com/ultralytics/ultralytics),  
which is also licensed under AGPL-3.0.

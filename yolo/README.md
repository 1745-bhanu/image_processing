# Object Detection using YOLOv5

## 📌 Project Overview
This project implements object detection using YOLOv5. The model is trained and tested on a custom dataset, and predictions are visualized.

## 📂 Dataset Preparation
To train a custom object detection model, you need to prepare your dataset in the correct structure:

1. **Create the dataset folder structure:**
    ```
    custom_dataset/
    ├── train/
    │   ├── images/      # Training images
    │   ├── labels/      # Corresponding YOLO annotation files (.txt)
    ├── validation/
    │   ├── images/      # Validation images
    │   ├── labels/      # Corresponding YOLO annotation files (.txt)
    ```

2. **Annotate Images Using Label Studio**  
   We need to create bounding box annotations for images.  
   - **Install Label Studio**:
     ```bash
     pip install label-studio
     label-studio
     ```
   - Open Label Studio in the browser, create a new project, and upload images.
   - Use the **Bounding Box tool** to annotate objects in the images.
   - **Export annotations in YOLO format** and move the `.txt` files to the corresponding `labels/` folder.

3. **Split Data into Train & Validation**  
   Ensure you divide your dataset into **train** and **validation** folders manually or using a script.

---

## 🔧 Installation
To set up this project, follow these steps:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/object_detection.git
    cd object_detection
    ```

2. **Create and Activate Virtual Environment** (Optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On macOS/Linux
    venv\Scripts\activate  # On Windows
    ```
    
## 🚀 Usage
To train the YOLOv5 model on your custom dataset, follow these steps:

1. Run the Jupyter Notebook:
    ```bash
    jupyter notebook
    ```
2. Open **`object_detection.ipynb`** and execute the cells sequentially.
3. Ensure your dataset is correctly placed in the `dataset/` folder.

## 🛠 Dependencies
Ensure you have the following installed:

- Python 3.8+
- Jupyter Notebook
- OpenCV
- PyTorch
- YOLOv5
- Matplotlib
- NumPy
- Label Studio (for annotation)

You can install the required packages with:

```bash
pip install opencv-python torch torchvision matplotlib numpy label-studio
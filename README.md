# License Plate Detection

This project is a Python script that detects and reads license plates from images using OpenCV for image processing and Tesseract OCR for text recognition. The script identifies a license plate in an image, extracts the region of interest, and outputs the detected text.

## Features

- Converts images to grayscale and applies Canny edge detection to find contours
- Identifies rectangular contours likely to be a license plate
- Applies image preprocessing (thresholding, noise reduction) for better OCR accuracy
- Uses Tesseract OCR to extract text from the detected license plate
- Draws a bounding box around the license plate and displays the extracted text on the image

## Prerequisites

- Python 3.x
- Tesseract-OCR installed on your system
- A sample image containing a visible license plate (e.g., `prsche.jpg`)

## Installation

### Install Tesseract-OCR:

- **Windows**: Download and install from [Tesseract-OCR](https://github.com/UB-Mannheim/tesseract/wiki). Note the installation path (default: `C:\Program Files\Tesseract-OCR\tesseract.exe`).
- **Linux**: Run `sudo apt-get install tesseract-ocr`.
- **macOS**: Run `brew install tesseract`.

Update the Tesseract path in `license_plate_detection.py` if necessary:
```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'  # Adjust for your system
```
### Clone the repository:

```bash
git clone https://github.com/your-username/License-Plate-Detection.git
cd License-Plate-Detection
```

### Install Python dependencies

```bash
pip install -r requirements.txt
```

### Add an Sample Image
-Place an image named prsche.jpg in the repository folder, or modify the script to point to your image:
```python
image = cv2.imread('your_image.jpg')
```

### Usage
--1.Ensure the image file (prsche.jpg or your own image) is in the repository folder.
--2,Run the script:

```bash
python license_plate_detection.py
```

### The script will:

-Load the image and convert it to grayscale.
-Apply Canny edge detection to find contours.
-Identify a rectangular contour as the potential license plate.
-Preprocess the license plate region (thresholding, noise reduction).
-Extract text using Tesseract OCR.
-Display three windows: the original image, the detected license plate, and the final image with a bounding box and extracted text.
-Print the detected license plate text to the console.
-Press any key to close the image windows.

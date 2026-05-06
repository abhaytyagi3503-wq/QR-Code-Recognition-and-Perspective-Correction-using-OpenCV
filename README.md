
# QR Code Recognition and Perspective Correction Using OpenCV

## Project Overview

This project focuses on generating, detecting, decoding, and correcting QR codes using Python and OpenCV. The main objective was to understand how QR code recognition works in computer vision and how image processing techniques can improve QR code readability under real-world conditions.

The project included QR code generation, QR code decoding, damage testing, perspective distortion, perspective correction, and final decoding verification. This helped demonstrate how OpenCV can be used to detect QR codes even when the image is partially damaged or viewed from an angle.

---

## Objectives

- Generate a QR code using Python.
- Decode the QR code using OpenCV.
- Test QR code robustness after partial damage.
- Create a tilted QR code using perspective distortion.
- Detect QR code corners using OpenCV.
- Apply perspective correction to restore the QR code view.
- Decode the corrected QR code successfully.

---

## Tools and Libraries Used

- Python 3
- OpenCV (`cv2`)
- NumPy
- `qrcode` library
- `pyzbar` for decoding verification

---

## Methodology and Project Execution

The project was completed through a step-by-step computer vision workflow. The main focus was to generate a QR code, test its readability, apply image distortion, correct the distorted image, and verify that the QR code could still be decoded.

### 1. QR Code Generation

A QR code was generated using the Python `qrcode` library. High error correction was used so that the QR code could remain readable even if a portion of the code was covered or damaged.

This step created the original QR code image that was used for all later testing.

---

### 2. QR Code Decoding Using OpenCV

The generated QR code was decoded using OpenCV’s built-in `QRCodeDetector`.

```python
import cv2

img = cv2.imread("example_qrcode.png")
qr = cv2.QRCodeDetector()

data, bbox, _ = qr.detectAndDecode(img)

print("Decoded QR:", data)
````

The purpose of this step was to confirm that the QR code was generated correctly and could be read by OpenCV.

---

### 3. QR Code Damage Test

To test robustness, a portion of the QR code was covered or erased. Since the QR code was generated with high error correction, it was still decoded successfully.

This demonstrated that QR codes can tolerate some missing or damaged regions while still preserving the encoded data.

---

### 4. Creating a Tilted QR Code

A perspective distortion was applied to the original QR code image to simulate a real-world situation where the QR code is viewed from an angle.

This step helped test how QR code recognition performs when the image is not perfectly aligned with the camera.

---

### 5. Perspective Correction

OpenCV was used to detect the corners of the tilted QR code. After detecting the corner points, a perspective transformation was applied to correct the distortion and restore the QR code to a front-facing view.

This step is important in computer vision because QR codes in real applications are often captured at an angle.

---

### 6. Decoding the Corrected QR Code

After perspective correction, the corrected QR code image was decoded again using OpenCV.

The successful decoding confirmed that the perspective correction process worked properly.

---

## How the System Works

```text
Generate QR Code
        ↓
Read QR Code Image
        ↓
Decode Using OpenCV QRCodeDetector
        ↓
Apply Damage Test
        ↓
Decode Damaged QR Code
        ↓
Apply Perspective Distortion
        ↓
Detect QR Code Corners
        ↓
Correct Perspective
        ↓
Decode Corrected QR Code
```

---

## Results and Outcomes

The project successfully demonstrated QR code recognition and correction using OpenCV.

Major outcomes included:

* Generated a readable QR code using Python.
* Decoded the QR code successfully using OpenCV.
* Verified that the QR code remained readable after partial damage.
* Created a tilted QR code using perspective distortion.
* Detected QR code corner points using OpenCV.
* Applied perspective correction to recover the QR code shape.
* Successfully decoded the corrected QR code.
* Demonstrated practical computer vision techniques for QR code detection and image correction.

---

## Key Features

* QR code generation
* OpenCV-based QR code detection
* QR code decoding
* Damage robustness testing
* Perspective distortion simulation
* Corner detection
* Perspective transformation
* Corrected QR decoding
* Python-based computer vision workflow

---

## Important Code Snippet

```python
import cv2

img = cv2.imread("example_qrcode.png")

qr = cv2.QRCodeDetector()
data, bbox, _ = qr.detectAndDecode(img)

print("Decoded QR:", data)
```

---

## Project Workflow

```text
Start Python Environment
        ↓
Install Required Libraries
        ↓
Generate QR Code
        ↓
Save QR Code Image
        ↓
Load Image Using OpenCV
        ↓
Detect and Decode QR Code
        ↓
Damage QR Code and Test Robustness
        ↓
Apply Perspective Distortion
        ↓
Correct Distorted QR Code
        ↓
Decode Corrected QR Code
```

---

## Repository Structure

```text
.
├── README.md
├── qr_code_recognition.py
├── example_qrcode.png
├── damaged_qrcode.png
├── tilted_qrcode.png
├── corrected_qrcode.png
└── output/
    └── qr_photos/
```

---

## How to Run the Project

### 1. Install Required Libraries

```bash
pip install opencv-python numpy qrcode pyzbar
```

### 2. Run the Python Script

```bash
python qr_code_recognition.py
```

### 3. Expected Output

The program should print the decoded QR code data in the terminal.

```text
Decoded QR: <QR code data>
```

It should also generate and save QR code images for the original, damaged, tilted, and corrected QR code cases.

---

## Applications

This project is useful for understanding QR code recognition in real-world computer vision applications such as:

* Mobile QR scanners
* Inventory tracking
* Robotics navigation markers
* Automated product identification
* Document verification
* Camera-based object tagging
* AR/VR marker detection

---

## Major Learnings

Through this project, I gained practical experience with:

* QR code generation using Python
* OpenCV QR code detection
* Image loading and processing
* Error correction behavior in QR codes
* Perspective distortion
* Perspective transformation
* Computer vision-based decoding
* Testing image robustness under damage and tilt conditions

---

## Conclusion

This project successfully implemented QR code recognition and perspective correction using Python and OpenCV. The QR code was generated, decoded, damaged, distorted, corrected, and decoded again to verify the complete workflow.

The project demonstrated how computer vision can be used to make QR code recognition more reliable under real-world conditions such as partial damage and angled camera views.

```
```

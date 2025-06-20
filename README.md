🧵 Cross Stitch Pattern Generator
A simple cross-stitch pattern generator based on uploaded images. The program automatically selects the closest colors from a DMC palette (or custom palette) and creates a pattern with color codes, symbols, and stitch count.



🔍 Main Features
Image Upload (JPG, PNG, BMP)
Automatic selection of optimal number of colors
Color matching using DMC or custom palettes
Pattern preview with grid and symbol overlay
Export to PNG and PDF formats
Custom palette management (import/export CSV)




🖼 Application Interface
The app is built with PyQt6 and consists of two main panels:

Left Panel:
Image Selection : "Select Image" button
Pattern Settings :
Width in stitches
Number of colors
Palette type: DMC or Custom
Custom Palette Management :
Add/remove DMC color by code
Save/load custom palette (CSV)
Actions : Preview, Generate Pattern
Right Panel:
Pattern Preview Area
Status Info : size, loading status




⚙️ Technical Details
Used Libraries:
PyQt6 — GUI interface
OpenCV (cv2) — image processing
scikit-learn (MiniBatchKMeans) — color clustering
matplotlib, PIL, numpy, pandas, skimage
Core Algorithm:
Load and resize image
Reduce to target number of colors via k-means clustering
Match clustered colors to nearest DMC color (CIEDE2000)
Generate enlarged pattern image with symbols and grid
Export pattern and legend to PDF






📦 How to Run
Requirements:
Python 3.8+
Install dependencies:
bash

pip install opencv-python scikit-learn matplotlib numpy pandas PyQt6 pillow

Launch:

python cross_stitch_generator.py


📄 Example Output
PDF output includes:

Enlarged pattern with symbols and grid
Color legend with DMC codes, names, and stitch counts

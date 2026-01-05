# Flipper Zero Animation Factory

A fully automated Python pipeline that converts standard GIF animations into Flipper Zero compatible asset packs. It handles resizing, dithering, `.bm` conversion, and manifest generation in a single batch process.

## 🚀 Features

* **Batch Processing:** Point it to a folder of GIFs, and it processes them all at once.
* **High-Quality Conversion**
* **Auto-Manifest Generation:**
    * Creates the required `meta.txt` for each animation.
    * Generates the master `manifest.txt` for the entire asset pack.
* **Preview Generation:** Creates a `_preview.gif` in every output folder so you can see the final 1-bit result instantly.
* **Clean Output:** Automatically converts PNGs to `.bm` (using `img2fbm`) and deletes the temporary files.

## 📋 Prerequisites

1.  **Python 3.x** installed.
2.  **img2fbm executable:**
    * This script requires the `img2fbm` tool to handle the final conversion to Flipper format.
    * Download `img2fbm.exe` (or your OS equivalent) from the [img2fbm repository](https://github.com/atomofiron/img2fbm).
    * **Place the `.exe` in the same folder as this script.**

## 📦 Installation

1.  Clone this repository or download the script.
2.  Install the required Python library (Pillow):
    ```bash
    pip install Pillow
    ```
3.  Ensure your directory looks like this:
    ```text
    /Project_Folder
    ├── script.py
    ├── img2fbm.exe
    ├── Input/          <-- Put your GIFs here
    └── Output/         <-- Results will appear here
    ```

## 🛠 Usage

### Batch Mode (Recommended)
To convert an entire folder of GIFs at once:
```bash

python script.py ".\Output" ".\Input"

# Automated Image Resizing and Cropping Suite for Entertainment Media

This repository contains a suite of automated scripts designed to resize and crop images, primarily aimed at optimizing workflows for entertainment media such as posters and still images. It is ideal for professionals handling large volumes of images, saving time while ensuring consistent quality. (Jupyter Notebook **`resize_and_crop_images.ipynb`**)

---

##  Why this script was created

In entertainment workflows, it's common to receive hundreds of original images that need to be resized and cropped into different dimensions (e.g., 600x900, 750x1120, 300x450, etc.) for different use cases like posters or stills.

Doing this manually — using Photoshop or another image editor — is not only repetitive and time-consuming but also error-prone, especially when consistent naming, cropping logic, and format compression are required.

This script automates the entire process, reducing a task that could take several hours or days into just a few minutes.

---

##  Features

- Resize original images to **one or multiple dimensions**
- **Center crop** (for Posters) or **Top + Center crop** (for Stills)
- 24-bit JPEG output with compression optimized for inflight systems
- Automatically renames and organizes files into folders by dimension and crop type
- Interactive and easy to use (just run from terminal and enter the parameters)

---

##  Estimated time saved

Manually processing images in Photoshop typically includes:  
opening, resizing, cropping, saving with compression, and renaming.

Let’s consider a common case:

- 200 original images  
- 4 output sizes per image  
→ Total: 800 final images

| Step                         | Manual (Photoshop)     | With this Script      |
|------------------------------|------------------------|------------------------|
| Time per image per version   | ~1 minute              | ~1 second              |
| Total time                   | 10–13 hours            | ~10–15 minutes         |
| Naming and folder structure  | Manual                 | Automatic              |
| Consistency and quality      | Varies                 | Standardized           |


In larger projects (e.g., 300 images across 8 dimensions = 2,400 final outputs), the time savings and reliability are even more significant.

---

## Requirements

- Python 3.x
- Pillow (`pip install Pillow`)

---

## How to use

1. Open the notebook `resize_and_crop_images.ipynb` in Jupyter or VSCode
2. Run all cells
3. Follow the interactive terminal prompts:
   - Enter the input folder (with original images)
   - Choose the output folder
   - Enter one or more dimensions (e.g., `600,900`)
   - Choose whether to generate center crop only (Poster) or both center and top crop (Still)

---

## Output structure

Depending on your selection, the structure will look like:

📁 output_folder/
- ├── 600x900/
- │ ├── Example1_600x900.jpg ← Center crop only
- │ ├── center_crop/
- │ │ └── Example1.jpg
- │ └── top_crop/
- │ └── Example1_600x900.jpg


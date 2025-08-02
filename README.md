# 🌀 CT Simulation & 3D Reconstruction Dashboard

Smart insights and interactive demos for 3D computed tomography (CT), built for exploration and learning.
- Simulate custom phantoms (disk, square, rectangle, triangle)
- Generate sinograms
- Reconstruct with SART (Simultaneous Algebraic Reconstruction Technique)
- View slice-by-slice or as a stack in 3D

---

### 🚀 Technologies Used

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=Jupyter)
![scikit-image](https://img.shields.io/badge/Scikit--image-%3E0.20-brightgreen?logo=python)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-purple)
![SART](https://img.shields.io/badge/SART-Reconstruction-yellow)

---

## 📦 Contents

- `notebooks/`: Jupyter notebooks for all code and demonstrations
  - `01-simulation-2D.ipynb` – 2D phantom creation, sinogram, SART
  - `02-3D-reconstruction.ipynb` – 3D stack demo & interactive exploration
- `images/`: Output/illustration images (optional)
- `README.md`: This documentation
- `requirements.txt`: List of Python dependencies

---

## 📚 What This Project Does

- **Create phantoms:** Disks, squares, rectangles, triangles—fully configurable in size & position
- **Simulate scans:** Generate sinograms (Radon transform) to replicate X-ray CT projections
- **Reconstruct images:** Perform iterative SART reconstruction for sharp, robust results
- **3D extension:** Stack slices to create realistic volumetric (3D) test objects
- **Visualize results:** Explore reconstructions with sliders, animations, or 3D viewers (e.g., napari)

---


## 💡 Methodology Overview

### Phantom Generation
- Shapes are generated as NumPy arrays for both 2D and as “stacks” for 3D volumes.
- Slices are varied to mimic true 3D structure (example: disk radius grows & shrinks, square’s center moves, triangle shifts laterally).

### Sinogram Creation
- Uses scikit-image’s `radon()` function to generate projection data across multiple angles—the CT “scan”.

### Reconstruction (SART)
- Sinograms are reconstructed into images or volumes using the `iradon_sart()` algorithm.
- SART provides noise robustness and works well with incomplete or limited-angle data.

### Visualization
- Middle and arbitrary slices visualized.
- Optional: interactive slice browsing (slider) or 3D render (via napari, see code snippets inside notebooks).

---

## ✨ Features Breakdown

- **Parameterizable:** Easily control phantom size, position, and per-slice variation.
- **Slice-by-slice 3D:** Not just 2D—phased per-slice change for realistic volume simulation.
- **SART technology:** Modern, robust iterative CT algorithm.
- **Interactive:** Use slidebars or animation for "scroll-through-slice" 3D effect.
- **Easy-to-read, modular code:** Clear functions for each major pipeline step.

---

## 🛠️ Requirements & Setup

- Python 3.7+
- numpy
- matplotlib
- scikit-image
- ipywidgets (for sliders)
- napari (optional, for 3D viewing)

---

## 📖 References

- [scikit-image Radon Transform docs](https://scikit-image.org/docs/stable/auto_examples/transform/plot_radon_transform.html)
- [Wikipedia: Radon Transform](https://en.wikipedia.org/wiki/Radon_transform)
- [Wikipedia: SART Algorithm](https://en.wikipedia.org/wiki/Simultaneous_algebraic_reconstruction_technique)
- [Mr. P Solver: CT Scans and Tomographic Recon in PYTHON (YouTube)](https://www.youtube.com/watch?v=qfAS8seVYvU)


---

## 🙌 Author

- Aryan Arvind Singh 
- National Tsing Hua University

---

**_Explore, learn, and visualize computed tomography—the code and the science!_**


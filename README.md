# Breakpoint AI - Tyler Bellenfant Demo
![breakpoint_logo](/static/logo.webp)

## Overview - Image Dataset Generation Project
This project is designed to create a diverse image dataset using inpainting techniques, leveraging the Stable Diffusion Inpainting Pipeline. It includes Python functions to generate image masks and automate the process of creating an object detection image dataset (YOLO Format) from a collection of base images and text prompts.
![example_outputs](/static/example_output.png)

## Features
1. Inpainting of images based on textual prompts.
2. Generation of masks for selective inpainting.
3. Automated creation of a labeled image dataset in YOLO format.

## Requirements
To run this project, you will need Python 3.10.x along with several dependencies listed in requirements.txt. It is recommended to use a virtual environment. Perform the Pytorch installation according to the official installation instructions for the version number listed in the requirements file and for your system configuration (https://pytorch.org/get-started/locally/). Then, install the remaining requirements using:

```bash
pip install -r requirements.txt
```

## Structure
```bash
breakpoint/
│
├── src/                      # Source code
│   ├── dataset_generator.py  # Main dataset generation script
│   ├── inpainting.py         # Inpainting functions
│   └── ...
│
├── data/                     # Data directory (input/output)
│   ├── input/                # Input images
│   └── output/               # Output images and bounding box files
│
├── notebooks/                # Jupyter notebooks for demos
│
├── requirements.txt          # Project dependencies
├── LICENSE                   # License information
└── README.md                 # Project overview (this file)
```

### Usage
To use this project, follow these steps:

Prepare your dataset: Place your input images in data/input/.
Set your prompts: Modify the prompts_classes_dict in src/dataset_generator.py with your desired prompts and corresponding classes.
Run the script: Execute dataset_generator.py to start generating the dataset.
Check the results: The output images and YOLO formatted label text files will be saved in data/output/.

## Notebooks
The notebooks/ directory contains Jupyter notebooks for demonstration and testing. These notebooks provide examples of how to use the functions in this project.

## License
The diffusion model weights are licensed under creativeml-openrail-m. The code is licensed under CC-BY-NC.

## Contact
For any queries or suggestions, please contact me here on Github.

## Citation
```
    @InProceedings{Rombach_2022_CVPR,
        author    = {Rombach, Robin and Blattmann, Andreas and Lorenz, Dominik and Esser, Patrick and Ommer, Bj\"orn},
        title     = {High-Resolution Image Synthesis With Latent Diffusion Models},
        booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
        month     = {June},
        year      = {2022},
        pages     = {10684-10695}
    }
```

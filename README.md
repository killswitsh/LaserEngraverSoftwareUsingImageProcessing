# Code README

This code provides functionality for image processing, SVG manipulation, and G-code generation. It includes several functions for resizing images, detecting contours, converting SVG paths to line segments, optimizing line distances, and generating G-code for laser engraving.

## Prerequisites

Before running the code, make sure you have the following dependencies installed:

- OpenCV (`cv2`)
- NumPy (`numpy`)
- svgpathtools (`svgpathtools`)
- tsp_solver (`tsp_solver`)
- Turtle graphics (`turtle`)
- tkinter (`tkinter`)
- svgwrite (`svgwrite`)
- PIL (`Pillow`)
- pyserial (`serial`)

You can install these dependencies using pip:

```bash
pip install opencv-python numpy svgpathtools tsp-solver turtle pyserial svgwrite pillow
```

## Usage
To use the code, follow these steps:

1. Import the necessary modules:
```python
import time
from xml.dom import minidom
import cv2
import numpy as np
import svgpathtools
from svgpathtools import svg2paths
from tsp_solver.greedy_numpy import solve_tsp
import turtle
from tkinter import *
from tkinter import filedialog
from PIL import Image, ImageTk
import serial.tools.list_ports
import tkinter.font as tkFont
import svgwrite
import tkinter as tk
```

2. Use the provided functions according to your requirements. The main functions in the code include:
```bash
resize_image_scale(image_path, scale_percent): Resizes the image based on a scale percent.
resize_image_width(image_path, target_width): Resizes the image based on a target width.
edited_image(img): Applies image processing techniques to extract contours from the image.
svgtolines(paths, attributes): Converts SVG paths to line segments.
optimize_line_distances(lines): Calculates a distance matrix that represents the distances between each pair of line segments.
gcode_generator(optimized_lines, laser_speed, laser_power, svg_dimensions): Generates G-code for laser engraving based on the optimized line segments.
get_image_width(image_path): Retrieves the width of an image.
get_image_height(image_path): Retrieves the height of an image.
main_start(): The main function that orchestrates the image processing, SVG manipulation, and G-code generation workflow.
```
3. Adjust the parameters and inputs within the main_start() function to suit your needs. This function serves as the entry point for executing the entire workflow.
4. Run the code by calling the main_start() function or the specific functions you want to use.




## Example
Here is an example of how to use the code:
```python
# Set the path to the input image
image_path = "input.jpg"

# Perform image processing, SVG manipulation, and G-code generation
main_start()
```
This will process the input image, generate an SVG file with the detected contours, optimize the line distances, and generate G-code for laser engraving.

## GUI
### Features

- Open and display an image
- Set laser power and speed
- Control the movement of the laser machine
- Reset the machine to its original position
- Virtualize button for testing purposes
### Troubleshooting
- If the application is not detecting your laser engraver machine, make sure it is properly connected and the correct serial port is specified in the code.

## Contributing
Contributions to the code are welcome. If you find any issues or have suggestions for improvements, please create an issue or submit a pull request on the GitHub repository.

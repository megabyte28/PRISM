# PRISM

Prism is a Python-based Image Analysis Dashboard. It takes any image as input and breaks it down into its core color components, generating a comprehensive 6-plot dashboard using Matplotlib.

![Prism Dashboard Demo](dashboard_demo.jpg)

About The Project-->

This script is a lightweight tool for visualizing the color profile of any image. It uses NumPy and Pandas to efficiently process every pixel and Matplotlib to create a rich, multi-plot dashboard.

The dashboard instantly reveals:
* The overall color balance (RGB).
* The most dominant color.
* The average color of the entire image.
* The distribution and range of intensities for each color channel.

Features:
The dashboard provides six key visualizations:

1.  Given Image: Displays the original input image.
2.  Color Distribution: A pie chart showing the total dominance of Red, Green, and Blue across all pixels.
3.  Average Color:A solid color block representing the average of all pixels.
4.  Red Pixelwise Intensity: A scatter plot of Red intensity (0-255) for every pixel.
5.  Green Pixelwise Intensity: A scatter plot of Green intensity (0-255) for every pixel.
6.  Blue Pixelwise Intensity: A scatter plot of Blue intensity (0-255) for every pixel.

The script also prints a simple "WARM" or "COOL" palette analysis to the console.

Tech Stack:
This project is built using:

* Python
* Matplotlib:For all data visualization and dashboard layout.
* Pandas:To structure pixel data into a DataFrame for easy analysis (like calculating means).
* NumPy:For high-performance array manipulation (reshaping, converting images to arrays).
* Pillow (PIL):For opening and loading the image files.

Getting Started: 
To get a local copy up and running, follow these simple steps.

Prerequisites:
You must have Python 3 and `pip` installed.

Installation:

1.  Clone this repository (or just download the `prism.py` file):

    git clone [https://github.com/megabyte28/prism.git](https://github.com/megabyte28/prism.git)

2.  Navigate to the project directory:
    
    cd prism
    
3.  Create a `requirements.txt` file with the following content:
    
    matplotlib
    numpy
    pandas
    Pillow
    
4.  Install the required packages:
    
    pip install -r requirements.txt
    
Usage:

1.  Place your image files (e.g., `sky.jpeg`, `spices.png`) in the same folder as the `prism.py` script.
2.  Open the `prism.py` script and scroll to the bottom.
3.  Change the function calls to match the names of your images:
    python
    # Call the dashboard function for your images
    dashboard("sky.jpeg")
    dashboard("spices.png")
    dashboard("nature.png")
    
4.  Run the script from your terminal:

    python prism.py
    
5.  A separate Matplotlib window will pop up for each image, displaying its complete analysis dashboard.

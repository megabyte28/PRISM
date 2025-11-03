<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prism - Image Analysis Dashboard</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            margin: 2rem auto;
            max-width: 800px;
            padding: 0 1rem;
            background-color: #fdfdfd;
            color: #333;
        }
        h1, h2 {
            border-bottom: 2px solid #eee;
            padding-bottom: 5px;
        }
        h1 {
            font-size: 2.5rem;
        }
        h2 {
            font-size: 1.8rem;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        code {
            font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
            background-color: #f6f8fa;
            padding: 0.2em 0.4em;
            margin: 0;
            font-size: 85%;
            border-radius: 6px;
        }
        pre {
            background-color: #f6f8fa;
            padding: 1rem;
            border-radius: 8px;
            overflow-x: auto;
        }
        pre code {
            padding: 0;
            margin: 0;
            font-size: 100%;
            background-color: transparent;
        }
        li {
            margin-bottom: 0.5rem;
        }
    </style>
</head>
<body>

    <h1>Prism --></h1>

    <p><strong>Prism</strong> is a Python-based Image Analysis Dashboard. It takes any image as input and breaks it down into its core color components, generating a comprehensive 6-plot dashboard using Matplotlib.</p>

    <img src="dashboard_demo.png" alt="Prism Dashboard Demo">

    <hr>

    <h2> About The Project</h2>
    <p>This script is a lightweight tool for visualizing the color profile of any image. It uses NumPy and Pandas to efficiently process every pixel and Matplotlib to create a rich, multi-plot dashboard.</p>
    <p>The dashboard instantly reveals:</p>
    <ul>
        <li>The overall color balance (RGB).</li>
        <li>The most dominant color.</li>
        <li>The average color of the entire image.</li>
        <li>The distribution and range of intensities for each color channel.</li>
    </ul>

    <hr>

    <h2> Features</h2>
    <p>The dashboard provides six key visualizations:</p>
    <ol>
        <li><strong>Given Image:</strong> Displays the original input image.</li>
        <li><strong>Color Distribution:</strong> A pie chart showing the total dominance of Red, Green, and Blue across all pixels.</li>
        <li><strong>Average Color:</strong> A solid color block representing the average of all pixels.</li>
        <li><strong>Red Pixelwise Intensity:</strong> A scatter plot of Red intensity (0-255) for every pixel.</li>
        <li><strong>Green Pixelwise Intensity:</strong> A scatter plot of Green intensity (0-255) for every pixel.</li>
        <li><strong>Blue Pixelwise Intensity:</strong> A scatter plot of Blue intensity (0-255) for every pixel.</li>
    </ol>
    <p>The script also prints a simple "WARM" or "COOL" palette analysis to the console.</p>

    <hr>

    <h2> Tech Stack</h2>
    <p>This project is built using:</p>
    <ul>
        <li><strong>Python</strong></li>
        <li><strong>Matplotlib:</strong> For all data visualization and dashboard layout.</li>
        <li><strong>Pandas:</strong> To structure pixel data into a DataFrame for easy analysis (like calculating means).</li>
        <li><strong>NumPy:</strong> For high-performance array manipulation (reshaping, converting images to arrays).</li>
        <li><strong>Pillow (PIL):</strong> For opening and loading the image files.</li>
    </ul>

    <hr>

    <h2> Getting Started</h2>
    <p>To get a local copy up and running, follow these simple steps.</p>

    <h3>Prerequisites</h3>
    <p>You must have Python 3 and <code>pip</code> installed.</p>

    <h3>Installation</h3>
    <ol>
        <li>Clone this repository (or just download the <code>prism.py</code> file).
            <pre><code>git clone https://github.com/YOUR_USERNAME/prism.git</code></pre>
        </li>
        <li>Navigate to the project directory:
            <pre><code>cd prism</code></pre>
        </li>
        <li>Create a <code>requirements.txt</code> file with the following content:
            <pre><code>matplotlib
numpy
pandas
Pillow</code></pre>
        </li>
        <li>Install the required packages:
            <pre><code>pip install -r requirements.txt</code></pre>
        </li>
    </ol>

    <hr>

    <h2> Usage</h2>
    <ol>
        <li>Place your image files (e.g., <code>sky.jpeg</code>, <code>spices.png</code>) in the same folder as the <code>prism.py</code> script.</li>
        <li>Open the <code>prism.py</code> script and scroll to the bottom.</li>
        <li>Change the function calls to match the names of your images:
<pre><code># Call the dashboard function for your images
dashboard("sky.jpeg")
dashboard("spices.png")
dashboard("nature.png")</code></pre>
        </li>
        <li>Run the script from your terminal:
            <pre><code>python prism.ipynb</code></pre>
        </li>
        <li>A separate Matplotlib window will pop up for each image, displaying its complete analysis dashboard.</li>
    </ol>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prism - Image Analysis Dashboard</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            margin: 2rem auto;
            max-width: 800px;
            padding: 0 1rem;
            background-color: #fdfdfd;
            color: #333;
        }
        h1, h2 {
            border-bottom: 2px solid #eee;
            padding-bottom: 5px;
        }
        h1 {
            font-size: 2.5rem;
        }
        h2 {
            font-size: 1.8rem;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
        }
        code {
            font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
            background-color: #f6f8fa;
            padding: 0.2em 0.4em;
            margin: 0;
            font-size: 85%;
            border-radius: 6px;
        }
        pre {
            background-color: #f6f8fa;
            padding: 1rem;
            border-radius: 8px;
            overflow-x: auto;
        }
        pre code {
            padding: 0;
            margin: 0;
            font-size: 100%;
            background-color: transparent;
        }
        li {
            margin-bottom: 0.5rem;
        }
    </style>
</head>
<body>

    <h1>Prism --></h1>

    <p><strong>Prism</strong> is a Python-based Image Analysis Dashboard. It takes any image as input and breaks it down into its core color components, generating a comprehensive 6-plot dashboard using Matplotlib.</p>

    <img src="dashboard_demo.png" alt="Prism Dashboard Demo">

    <hr>

    <h2> About The Project</h2>
    <p>This script is a lightweight tool for visualizing the color profile of any image. It uses NumPy and Pandas to efficiently process every pixel and Matplotlib to create a rich, multi-plot dashboard.</p>
    <p>The dashboard instantly reveals:</p>
    <ul>
        <li>The overall color balance (RGB).</li>
        <li>The most dominant color.</li>
        <li>The average color of the entire image.</li>
        <li>The distribution and range of intensities for each color channel.</li>
    </ul>

    <hr>

    <h2> Features</h2>
    <p>The dashboard provides six key visualizations:</p>
    <ol>
        <li><strong>Given Image:</strong> Displays the original input image.</li>
        <li><strong>Color Distribution:</strong> A pie chart showing the total dominance of Red, Green, and Blue across all pixels.</li>
        <li><strong>Average Color:</strong> A solid color block representing the average of all pixels.</li>
        <li><strong>Red Pixelwise Intensity:</strong> A scatter plot of Red intensity (0-255) for every pixel.</li>
        <li><strong>Green Pixelwise Intensity:</strong> A scatter plot of Green intensity (0-255) for every pixel.</li>
        <li><strong>Blue Pixelwise Intensity:</strong> A scatter plot of Blue intensity (0-255) for every pixel.</li>
    </ol>
    <p>The script also prints a simple "WARM" or "COOL" palette analysis to the console.</p>

    <hr>

    <h2> Tech Stack</h2>
    <p>This project is built using:</p>
    <ul>
        <li><strong>Python</strong></li>
        <li><strong>Matplotlib:</strong> For all data visualization and dashboard layout.</li>
        <li><strong>Pandas:</strong> To structure pixel data into a DataFrame for easy analysis (like calculating means).</li>
        <li><strong>NumPy:</strong> For high-performance array manipulation (reshaping, converting images to arrays).</li>
        <li><strong>Pillow (PIL):</strong> For opening and loading the image files.</li>
    </ul>

    <hr>

    <h2> Getting Started</h2>
    <p>To get a local copy up and running, follow these simple steps.</p>

    <h3>Prerequisites</h3>
    <p>You must have Python 3 and <code>pip</code> installed.</p>

    <h3>Installation</h3>
    <ol>
        <li>Clone this repository (or just download the <code>prism.py</code> file).
            <pre><code>git clone https://github.com/YOUR_USERNAME/prism.git</code></pre>
        </li>
        <li>Navigate to the project directory:
            <pre><code>cd prism</code></pre>
        </li>
        <li>Create a <code>requirements.txt</code> file with the following content:
            <pre><code>matplotlib
numpy
pandas
Pillow</code></pre>
        </li>
        <li>Install the required packages:
            <pre><code>pip install -r requirements.txt</code></pre>
        </li>
    </ol>

    <hr>

    <h2> Usage</h2>
    <ol>
        <li>Place your image files (e.g., <code>sky.jpeg</code>, <code>spices.png</code>) in the same folder as the <code>prism.py</code> script.</li>
        <li>Open the <code>prism.py</code> script and scroll to the bottom.</li>
        <li>Change the function calls to match the names of your images:
<pre><code># Call the dashboard function for your images
dashboard("sky.jpeg")
dashboard("spices.png")
dashboard("nature.png")</code></pre>
        </li>
        <li>Run the script from your terminal:
            <pre><code>python prism.ipynb</code></pre>
        </li>
        <li>A separate Matplotlib window will pop up for each image, displaying its complete analysis dashboard.</li>
    </ol>

</body>
</html>
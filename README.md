# Extract data from MS data and plot
Written by Kelly Styles, 13th November 2024

## Introduction
This Jupyter Notebook is intended to be used to aid in the preparation of publication quality figures of LC-MS data. 
For each MS data file in a target directory, it will prepare a subplot for each file and plot a line for each of the 
specified target masses; producing a plot similar to a Mestrenova stacked chromatogram plot. This Notebook will save the 
hassle of having to load the data into Mestrenova, extracting each EIC, sending these to separate plots, then stacking those. 
It also provides a fairly repeatable method to generate these figures.

## Installation
In order to use this Notebook you will need to prepare a conda environment containing the following non-standard Python libraries:
- pyopenms (tested on version 3.2.0)
- seaborn (tested on version 0.11.2)
- gradio (tested on version 5.1.0)

💡 **Note:** *The easiest way to do this is to install Anaconda for Windows/Mac OS and 
  prepare an environment containing these packages. Then launch Jupyter Lab/Jupyter Notebook from this environment.*

Alternatively, you could try running the code in the next cell in this notebook. You might need to restart the kernel after this 
to load these newly installed libraries (i.e., `Kernel > Restart Kernel...`).

## Preparing your MS data

You will need to convert your existing vendor MS files to the `mzXML` or `mzML` formats. 
For Agilent data for example, you will need to:
1. Convert your Agilent '.D' files to MassHunter format using the 'LC-SQ ChemStation Translator' software provided by Agilent.
2. Convert this data to mzXML format using [Proteowizard - msConvert](https://proteowizard.sourceforge.io/download.html)

💡 **Note:** *This Notebook will work for both MS1 and MS2 files, but only extracting MS1 data from the latter.*

## Usage
💡 **Note:** *Make sure to click `Run > Run All Cells` in the Notebook to launch the GUI!*

Up the top of Jupyter Notebook/Lab, click `Run > Run All Cells` and a new window should pop up in your browser. Upload your `mzXML` 
files in the order you would like them to be plotted, then input your selected parameters and play around with image output options. 
Both SVG and JPG image files will be generated for each plot and can be foung in the same folder as this Notebook.

![Upload your MS files and input your masses / colours / label names](https://github.com/user-attachments/assets/c1e7db32-d781-4c5b-9c62-f2a2fbf33722)
![Input your plotting options](https://github.com/user-attachments/assets/e5f21bc1-8295-427d-b566-f0f21e942d2d)
![Output image](https://github.com/user-attachments/assets/18b208df-bc27-4bcb-9e8f-3c2f6a026fab)

## Troubleshooting
Several issues could cause an `Error` message. First check if using labels that the filenames in the table match the filename in the 
uploaded files section, sometimes extra spaces might appear if these are copied and pasted. If using LaTeX formatting syntax for the 
label names, check this is also correct. Also, if using named colours, check these are spelled correctly. If none of these are relevant, 
there will likely be some error messages at the bottom of this Notebook. Copy and paste this and pass it on to me and I can try to see 
what's going on.


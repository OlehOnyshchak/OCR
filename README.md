# Optical Character Recognition(OCR) system for math expressions
## Abstract
OCR is one of the earliest addressed computer vision tasks. But there are few solutions available for its application in specific domains such as parsing of mathematical formulas. Thus we will solve this problem in a simple educative way, providing a comprehensive introduction into Computer Vision(CV) field with a possibility to extend the base solution. The resulting program incorporates segmentation of input image into characters and then character recognition itself based on Convolutional Neural Network(CNN).
## Reproduce results
Firstly, prepare the data by executing the following commands from the project's root folder:
```
cd data
unzip emnist.zip
unzip crohme.zip
```
And then run `Main.ipynb` notebook
## Files Description
In the root folder, you can see multiple `*.ipynb` and `*.py` files. Below is a detailed description of each of them
* **References.ipynb** - notebook with reference materials related to the project,
* **Troubleshooting.ipynb** - notebook with a list of typical problems, which you may encounter while running the project, and their resolutions
* **DataPreprocessing.ipynb** - notebook for preprocessing datasets. It cleans, merges and enhances data from EMNIST and CHRONME datasets, which located under `data` directory
* **CharacterSegmentation.py** - python module with realisation of line segmentation functionality. It takes its input from the `input` folder and saves the segmented characters into `segmented` folder.
* **RecognitionModelTraining.ipynb** - notebook which trains CNN model to parse characters. Trained models are saved under the `model` directory.
* **Main.ipynb** - notebook with a main pipeline of the project. It orchestrates all modules by firsly segmenting the line into characters, then parsing them, and then converting parsed characters to Latex.

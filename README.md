# Celestial Seeker

**Celestial Seeker** is a collection of automated pipeline in python made to process FITS files that have astronomical imagery and detect celestial objects such as stars, planets, or galaxies, along with satellite position and orbit tracking around the Earth.

## Detailed Problem Statement

### Task 1

Design a modular pipeline that performs the following steps:
1. Data Ingestion: Read satellite imagery from FITS files.
2. Image Processing: Detect and identify clusters of bright pixels representing celestial
objects.
3. Feature Extraction: Measure object properties such as position, size, and luminosity.
4. Data Output: Save the processed results into a CSV file for further analysis.

### Task 2

Create a Python program that:
1. Parses TLE data for a given satellite.
2. Predicts the satellite's position (latitude, longitude, altitude) over a specified time range.
3. Visualizes the orbital trajectory using a 3D plot.

## How to use the notebooks with your own data

### Training Notebook: Task 1

1. Fork the notebook using the kebab menu on the top right corner of the notebook page and selecting `Copy & Edit Notebook`.
2. If you have another dataset consisting of your own labels of astronomical objects, upload it to your kaggle notebook using Kaggle's GUI.
3. Set the `input_dir` variable to the directory of your input dataset.
4. In case you want to train for a different number of epochs, in the call for the function `train_model`, add the parameter `num_epochs` with value equal to your desired epoch number.
5. Run the notebook to obtain your version of the trained model.

### Validation Notebook: Task 1

1. Fork the notebook using the kebab menu on the top right corner of the notebook page and selecting `Copy & Edit Notebook`.
2. If you have another dataset consisting of your your own fits file to infer from, or your own version of the VGG 16 model obtained from the above process, upload it to your kaggle notebook using Kaggle's GUI.
3. In the main portion of the first codeblock, set the `fits_path` variable equal to the fits file that you uploaded.
4. On running the first codeblock, obtain the image file from `/kaggle/working/saved_images/`.
5. Run the second codeblock without any changes
6. Paste your image path to the `image_path` variable of the last codeblocks.
7. Set the parameter of `torch.load()` invocation equal to the path to your trained VGG 16 model.
8. Run the codeblock to obtain the inference output.

### Task 2

For using your own TLE data, just set the `tle_data` equal to the new values. Run the notebook to get your output along with visualization.

## Kaggle Notebooks

- https://www.kaggle.com/code/dhriti1015/notebook915deae905/edit/run/215274045
- https://www.kaggle.com/code/invincible13/astro-object-detector
- https://www.kaggle.com/code/invincible13/celestial-obj-det-tester

## [Complete documentation](https://docs.google.com/document/d/1mUzES6FWD6KJJfoBMnRtITORi_JXgZxSDHwPkrZrCd0/edit?usp=sharing)

## References
- [VGG 16 Research Paper](https://arxiv.org/pdf/1409.1556)
- [Training a VGG 16 model](https://www.analyticsvidhya.com/blog/2021/06/transfer-learning-using-vgg16-in-pytorch/)
- [AlexNet Weight Documentation](https://pytorch.org/vision/main/models/generated/torchvision.models.alexnet.html)
- [Astropy Documentation](https://docs.astropy.org/en/stable/index.html)
- [Scikit Image Documentation](https://scikit-image.org/docs/stable/)
- [Nasa Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/)
- [STScI (Hubble Legacy Archive)](https://hla.stsci.edu/)
- [NOIRLab Astro Data Archive](https://astroarchive.noirlab.edu/)
- [Data-driven satellite orbit prediction using two-line elements](https://www.sciencedirect.com/science/article/abs/pii/S2213133723000975)
- [Satellite Maneuver Detection Using Two-line Element (TLE) Data](https://amostech.com/TechnicalPapers/2007/Modeling_Analysis_Simulation/Kelecy.pdf)
- [SGP4 Model PyPI](https://pypi.org/project/sgp4/) 
- [Simplified Approach to Detect Satellite Maneuvers Using TLE Data and Simplified Perturbation Model Utilizing Orbital Element Variation](https://www.mdpi.com/2076-3417/11/21/10181)
- [Two-Line Elements (TLE)](https://spire.com/spirepedia/two-line-elements-tle/#:~:text=The%20TLE%20format%20was%20developed,of%20two%20lines%20of%20text.)
- [Detailed Description of “Two-Line Element (TLE)” Orbital Parameters](https://onlinelibrary.wiley.com/doi/pdf/10.1002/9781119413585.app5)
- [Improved SSA Through Orbit Determination of Two-Line Element Sets](https://conference.sdo.esoc.esa.int/proceedings/sdc6/paper/153)
- [UK – Definitions: Event parameter](https://www.monitor-your-satellites.service.gov.uk/page/definitions)

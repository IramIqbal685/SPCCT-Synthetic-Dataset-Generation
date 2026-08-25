# Physics-Informed Synthetic Dataset Generation for Rock Material Decomposition and Identification using Spectral Photon Counting Computed Tomography (SPCCT)
## Overview
This repository contains the code developed for generating physics-informed synthetic Spectral Photon-Counting Computed Tomography (SPCCT) data for rock material analysis.

The repository includes four main workflows:
1. **LAC Calculation.ipynb** – calculation of material properties, including density, effective atomic number (Zeff), linear attenuation coefficients (LAC) using NIST XCOM data and Calibration & Gaussian Distribution Parameters. 
2. **Dataset Generation.ipynb** – generation of multi-energy synthetic SPCCT images using weighted LAC (wLAC) values and material probabilities provided in the Excel file `GD with inverse calibrated wLAC`.
3. **Zeff and ED Map.ipynb** – calculation of Effective Atomic Number (Zeff) and Electron Density (ED) maps from the generated synthetic SPCCT images.
4. **Rock Digital Phantom.ipynb** – generation of a synthetic rock digital phantom using the same material parameters, followed by Zeff and ED map calculation.

## Repository Supporting Files
- `Compounds.xlsx`  
  Input file containing the material compounds, its corresponding elements, densties and Mass fraction to calculate the Effective Atomic Mass, Effective Atomic Number, Electron Density, weighted LAC and Calibration Parameters along with Gaussian Distribution parameters for the compounds.

- `Spectrum_df.xlsx`  
  Input file containing X-ray spectrum of number of photons at each energy point to calculated the weighted Linear attenuation corfficient.
  
- `GD with inverse calibrated wLAC.xlsx`  
  Input file containing the material compounds, inverse-calibrated weighted LAC values for the five energy bins, and material probabilities for Dataset Generation & Rock Digital Phantom.

## Requirements
The code was developed in Python using Jupyter Notebook/Google Colab.

**Required packages:**
numpy
pandas
scipy
scikit-image
tifffile
matplotlib
openpyxl

## Expected Outputs
The workflows generate:
Five-bin synthetic SPCCT images
Material label maps
Synthetic Rock digital phantom
Effective Atomic Number (Zeff) maps
Electron Density (ED) maps
Validation and statistical output files

## Data Availability
The repository contains the source code required to reproduce the computational workflow. Large generated synthetic datasets and external characterization data are not necessarily included in the repository. Input data that are subject to confidentiality, usage restrictions, or size limitations may be provided separately where permitted.

## Citation
If you use this code, please cite the associated publication:
Physics-Informed Synthetic Dataset Generation for Rock Material Decomposition and Identification using Spectral Photon-Counting Computed Tomography. Publication details will be added after acceptance.

## Authors
Iram Iqbal and co-authors.

## Contact
For questions regarding the code or research, please contact the corresponding author associated with the related publication.

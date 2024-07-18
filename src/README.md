# High-Energy Physics Deep Learning Project

## Overview

This project explores the application of deep learning techniques in high-energy physics using data from the CMS experiment at the LHC. The repository includes analyzers, scripts, and notebooks to process collision data and train convolutional neural networks (CNNs) for particle classification.

## File Descriptions

### Analyzers

- **JetAnalyzer.cc**
  - Description: Analyzer for processing jet data.

- **MetAnalyzer.cc**
  - Description: Analyzer for processing missing transverse energy (MET) data.

- **MuonAnalyzer.cc**
  - Description: Analyzer for processing muon data. Configured to extract gen-level information.

- **MuonAnalyzer_realdata.cc**
  - Description: Analyzer for processing real muon data from CMS Open Data. Used in the final version of the CMS Open Data Workshop 2022.

### Scripts

- **poet_reduced.py**
  - Description: Script configured to work with `MuonAnalyzer.cc` for extracting gen-level information.

- **poet_realdata.py**
  - Description: Script designed to work with `MuonAnalyzer_realdata.cc` for processing real muon data.

### Notebooks

- **cnnmodel.ipynb**
  - Description: Jupyter notebook for training and evaluating CNN models on generated images from collision data.

- **image_generator_imass_script.ipynb**
  - Description: Jupyter notebook for generating images from collision data and calculating invariant mass distributions.


## Usage

1. **Data Analysis:**
   - Use `JetAnalyzer.cc`, `MetAnalyzer.cc`, `MuonAnalyzer.cc`, and `MuonAnalyzer_realdata.cc` to process jet, MET, and muon data.
   - `poet_reduced.py` should be used with `MuonAnalyzer.cc` for gen-level data analysis.
   - `poet_realdata.py` should be used with `MuonAnalyzer_realdata.cc` for real data analysis.

2. **Image Generation and Model Training:**
   - Use `image_generator_imass_script.ipynb` to generate images from the processed data.
   - Train and evaluate CNN models using `cnnmodel.ipynb`.

## References

1. CERN — LHC images gallery. Available at: [CERN Resources](https://home.cern/resources/image/accelerators/lhc-images-gallery)
2. Izaak Neutelings. CMS coordinate system. Available at: [TikZ CMS](https://tikz.net/axis3d_cms/)
3. C. F. Madrazo, I. H. Cacha, L. L. Iglesias, and J. M. de Lucas, “Application of a convolutional neural network for image classification to the analysis of collisions in high energy physics,” CoRR, vol. abs/1708.07034, 2017.
4. “Ochoa, J. D. CNN-hep-thesis: Undergrad Thesis. Using a CNN to classify different HEP processes. GitHub. Available at: [GitHub](https://github.com/jose8af/cnn-hep-thesis)
5. Merizalde, D., Ochoa, J., Tintin, X., Carrera, E., Martinez, D., Mena, D. (2023). Exploring the Performance of Deep Learning in High-Energy Physics. In: Maldonado-Mahauad, J., Herrera-Tapia, J., Zambrano-Martínez, J.L., Berrezueta, S. (eds) Information and Communication Technologies. TICEC 2023. Communications in Computer and Information Science, vol 1885. Springer, Cham. [https://doi.org/10.1007/978-3-031-45438-7_3](https://doi.org/10.1007/978-3-031-45438-7_3)

---

Thank you very much!

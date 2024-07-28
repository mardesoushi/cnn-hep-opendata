# Exploring the Performance of Deep Learning in High-Energy Physics

**Authors:** José Ochoa, Daniela Merizalde, Xavier Tintin, Edgar Carrera, Diana Martínez, David Mena  
**Date:** 10-18-2023  
**Affiliation:** Universidad San Francisco de Quito


To run GitHub project notebooks in Google Colab, follow these simplified steps:

1. **Access Google Colab**: Open [Google Colab](https://colab.research.google.com) in your browser and sign in with your Google account.

2. **Connect to the GitHub Repository**: In Colab, go to **File** > **Open notebook** > **GitHub**. Enter `xaviertintin/cnn-hep-thesis` directly in the search box, and press the search icon to connect to the correct repository.

3. **Open the Notebook**: Select the repository `src/cnnmodel.ipynb` from the `main` branch, and the Jupyter notebook you want to open.

4. **Run the Notebook**: Once open, run the notebook cells as you would in a local Jupyter environment.


## Table of Contents

1. Introduction
2. Methodology
3. Results
4. Conclusions

## Introduction

### The Universe We See and How to "Break" It
High-energy physics explores the fundamental particles and forces that constitute the universe. Through experiments like those conducted at the Large Hadron Collider (LHC), scientists can probe these building blocks by accelerating particles to near light speeds and colliding them, revealing the underlying physics.

### LHC and CMS
The LHC at CERN is a world-leading particle accelerator that conducts high-energy collisions. The Compact Muon Solenoid (CMS) is one of the general-purpose detectors at the LHC. It is designed to detect a wide range of particles and phenomena produced in collisions.

### A Physics Process
Collisions at the LHC produce a variety of particles and interactions. Understanding these processes helps to explore theories beyond the Standard Model of particle physics.

### The DHJW Scenario
This scenario includes processes such as:
- Drell-Yan
- Higgs
- \( J/\psi \)
- \( W \) + jets

### The DTW Scenario
This scenario includes:
- Drell-Yan
- \( W \) + jets
- \( t\bar{t} \) + jets

## General Approach

1. Extract relevant information from the CERN Open Data Portal.
2. Use that information to generate images for two scenarios (DHJW and DTW).
3. Train various Convolutional Neural Networks (CNNs) using these images.
4. The trained neural network with the best performance is used to classify real collision data.

## Methodology

### Data Collection and Information Extraction
The datasets used correspond to the simulation and real data obtained in 2015 during CMS Run II at 13 TeV. The focus is on:
- Muons
- Jets
- Missing Transverse Energy (MET)

### Image Generation
Images were generated for two scenarios: DHJW and DTW, with details such as the number of jets and presence of MET or muon charge information varying between them.

### Types of Neural Network
Evaluating CNN architectures:
- ResNet 50
- DenseNet
- InceptionV3
- MobileNet V2

Each model’s accuracy, loss, and F1 score were evaluated to determine the most suitable model for classifying high-energy particle collision outcomes.

### Training Process and Evaluation Metrics
- Training over 40 epochs with early stopping.
- Using Adam optimization algorithm and Softmax Loss.
- Training and testing conducted on Google Colaboratory using A100 GPU hardware accelerators.
- Code available at: [GitHub](https://github.com/jose8af/cnn-hep-thesis)

## Results

### Performance Metrics
The performance metrics, including accuracy and loss values, were evaluated for both the DHJW and DTW datasets. The confusion matrices of the best models for each scenario were analyzed.

### Application of the Model in Real Collision Data
The trained models were applied to real collision data, and the results, such as the dimuon invariant mass predictions, were compared to the actual collision data.

## Conclusions

- Promising results were obtained for both DHJW and DTW scenarios with accuracies greater than 80%.
- ResNet50 demonstrated the best performance among the evaluated CNN models.
- The DTW model could differentiate the Z boson resonance from a collection of real collision data.

## References

1. Merizalde, D., Ochoa, J., Tintin, X., Carrera, E., Martinez, D., Mena, D. (2023). Exploring the Performance of Deep Learning in High-Energy Physics. In: Maldonado-Mahauad, J., Herrera-Tapia, J., Zambrano-Martínez, J.L., Berrezueta, S. (eds) Information and Communication Technologies. TICEC 2023. Communications in Computer and Information Science, vol 1885. Springer, Cham. [https://doi.org/10.1007/978-3-031-45438-7_3](https://doi.org/10.1007/978-3-031-45438-7_3)

2. CERN — LHC images gallery. Available at: [CERN Resources](https://home.cern/resources/image/accelerators/lhc-images-gallery)
3. Izaak Neutelings. CMS coordinate system. Available at: [TikZ CMS](https://tikz.net/axis3d_cms/)
4. C. F. Madrazo, I. H. Cacha, L. L. Iglesias, and J. M. de Lucas, “Application of a convolutional neural network for image classification to the analysis of collisions in high energy physics,” CoRR, vol. abs/1708.07034, 2017.
5. “Ochoa, J. D. CNN-hep-thesis: Undergrad Thesis. Using a CNN to classify different HEP processes. GitHub. Available at: [GitHub](https://github.com/jose8af/cnn-hep-thesis)”

---

Thank you very much!

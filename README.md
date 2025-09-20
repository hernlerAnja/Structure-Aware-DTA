# Structure-Aware TankBind Embeddings for Drug-Target Affinity Prediction
Bachelor Thesis Project at JKU

---

## Overview

This repository contains the code for the bachelor thesis “Structure-Aware TankBind Embeddings for Drug–Target Affinity Prediction”.

Predicting drug–target binding affinity (DTA) is a crucial step in early-stage drug discovery, allowing researchers to prioritize promising compounds and reduce experimental costs. Traditional computational approaches, which rely on sequence- or graph-based representations of drugs and proteins, often fail to fully capture the three-dimensional structural context of molecular interactions.

This project leverages structure-aware latent embeddings extracted from a pre-trained TankBind model as input features for downstream DTA prediction on the KIBA dataset. While TankBind alone exhibits limited generalization on KIBA, its latent representations encode rich geometric and biochemical information about protein–ligand interactions. By preprocessing KIBA to retrieve protein structures, predict binding pockets, and extract ligand and protein features, these embeddings are used to train predictive models such as MLP, XGBoost, and LightGBM.

---

## Technologies Used

- Python 3.8
- Jupyter Notebook
- DeepPurpose - deep learning library for drug-target interaction prediction ([installation guide](https://github.com/kexinhuang12345/DeepPurpose))
  - Note: The installation guide in the repository did not work for me. After some trial and error, I got it running with: 
  
  ```bash
  pip install DeepPurpose
  ```

  However, this only worked on Windows 10. On Windows 11, I was unable to get it working.
- P2Rank - protein-ligand binding site prediction tool ([setup guide](https://github.com/rdk/p2rank))
- TankBind - reused code snippets and methodology ([GitHub repo](https://github.com/luwei0917/TankBind))

---

## Installation

Clone this repository and create the environment from `environment.yml`:

```bash
git clone https://github.com/hernlerAnja/Structure-Aware-DTA.git
cd Structure-Aware-DTA
conda env create -f environment.yml
conda activate tankbind-env
```

For DeepPurpose and p2rank, please refer to the official installation/setup guides linked above.

---

## Usage

All experiments and analysis are contained within Jupyter Notebooks. To run them:

```bash
jupyter notebook
```

**Note on third-party tools:**

If the installation of DeepPurpose od p2rank fails or is not working on your system, you can still run everythin in this repository except for `Load_Process_KIBA.ipynb`. That notebook only contains the preprocessing pipeline.

- The final processed data and all intermediate dataframes are already saved in the repository.
- This makes the project independent of those tools for running the main experiments.

---

## License

This project is licensed under the [MIT License](LICENSE)

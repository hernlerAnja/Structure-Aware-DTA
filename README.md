# Structure-Aware TankBind Embeddings for Drug-Target Prediction
Bachelor Thesis Project at JKU

---

## Overview

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
git clone 
cd 
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
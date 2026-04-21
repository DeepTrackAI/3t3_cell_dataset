# 3T3 Cell in AFM Dataset (3t3_cell_dataset)

## Overview

This DeepTrackAI repository replicates part of the **3T3 Cell in AFM Dataset**, consisting of AFM force spectroscopy data collected using the 3T3 cell.

These data were used for developing quality control technology for AFM force spectroscopy data based on the variational autoencoder.

Each force spectroscopy test contains:
- **Approach part**: Vertical tip position (µm) and vertical deflection (nN) collected in the approach process.
- **Retraction part**: The same variables as previous term that are collected in the retraction part.
- **Contact Point**: Contact point(µm) estimated by Hertz model, based on the approach part.
- **Young's Modulus**: Young's modulus (Pa) estimated by Hertz model, based on the approach part.
- **Data Quality Label**: only for the approach part, `0` is the good curve, `1` is the bad one, and `-1` is unknown.

### Summary
- **Number of force spectroscopy tests**: 2548
- **Number of curves per test**: 2, one for the approach part, one for the retraction part
- **Number of contact points per test**: 1, based on approach part
- **Number of Young's modulus per test**: 1, based on approach part
- **Number of labels for data quality per test**: 1, only for approach part
- **Data size**: variable, depending on the topology of cell sample
- **Data format**: 64-bit float number for force spectroscopy data, contact point, and Young's modulus, 8-bit integer number for label data

---

## Original Source

- **Title**: 
- **Authors**: Nazli Demirpehlivan, Rachel Owen (Bruker Nano Gmbh)
- **Source**: This repository
- **Reference article**: 
- **License**: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

If you use this dataset in your research, please follow the licensing requirements and properly attribute the original authors.

---

## Dataset Structure

```bash
/3t3_cell_dataset  
  ├── approach\               # Approach curves.
  │   ├── <filename_1>.npy
  │   ├── <filename_2>.npy  
  │   └── ...  
  ├── retraction\             # Retraction curves.
  │   ├── <filename_1>.npy  
  │   ├── <filename_2>.npy  
  │   └── ...  
  ├── contact_point.npy       # Contact point estimated by Hertz model.
  ├── young_modulus.npy       # Young's modulus estimated by Hertz model.
  └── label.npy               # Data quality labels for approach curves.

```

The file format, `.npy`, is powered by the `NumPy` package in Python. Each curvers in the two `.pkl` files are paired, as they are collected in one test including both the approach and retraction process. Also, the order of the labels/contact points/Young's modulus is consistent with the curve.

---

## How to Access the Data

### Clone the Repository
```bash
git clone https://github.com/DeepTrackAI/3t3_cell_dataset
cd 3t3_cell_dataset
```

---

## Attribution

If you use this dataset, please cite both the 3T3 Cell in AFM dataset repository and the reference article.

### Cite the dataset:
placeholder

```bibtex
@misc{,
  title={},
  author       = {},
  year         = {},
  howpublished = {\url{https://github.com/DeepTrackAI/3t3_cell_dataset}}
}
```

### Cite the reference article:
placeholder

```bibtex
@article{,
  title={},
  author={},
  journal={},
  volume={},
  number={},
  pages={},
  year={},
  publisher={},
  doi={}
}
```

---

## License

This dataset is shared under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

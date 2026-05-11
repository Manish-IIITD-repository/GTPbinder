# GTPbinder: Identification of GTP-Interacting Residues

Welcome to the official documentation for **GTPbinder**, a specialized computational tool developed for the prediction and identification of GTP-binding residues in protein sequences. GTP-binding proteins (G-proteins) are essential molecular switches in cellular processes, including signal transduction, protein synthesis, and intracellular trafficking.

**Web Server:** (https://webs.iiitd.edu.in/raghava/gtpbinder/) 

---

## Citation

Chauhan JS, Mishra NK, Raghava GPS (2010).  
**Prediction of GTP interacting residues, dipeptides and tripeptides in a protein from its evolutionary information.** *BMC Bioinformatics*, 11, 301.  
[https://doi.org/10.1186/1471-2105-11-301](https://doi.org/10.1186/1471-2105-11-301) 
Zenodo:-(https://doi.org/10.5281/zenodo.20069401)

---

## About the Platform

GTPbinder was developed to assist researchers in identifying residues that interact with Guanosine Triphosphate (GTP). Since GTP-binding proteins often share low sequence similarity despite structural conservation, this platform utilizes evolutionary information in the form of Position-Specific Scoring Matrices (PSSM) to achieve high predictive accuracy.

The platform is designed to:
* **Annotate Proteomes**: Identify potential GTP-binding sites in newly sequenced proteins .
* **Understand Mechanisms**: Elucidate the structural and sequence requirements for GTP interaction .
* **Support Drug Design**: Identify target residues for small-molecule inhibitors in signaling pathways .

---

## Key Features

### Predictive Modeling
* **Machine Learning**: Built using Support Vector Machines (SVM) optimized with the RBF kernel .
* **Evolutionary Profiles**: Utilizes PSI-BLAST generated PSSM profiles to capture residue conservation at interacting sites .
* **High Performance**: 
    * **Single Sequence Mode**: Achieved an accuracy of 70.81% and MCC of 0.42 .
    * **PSSM Profile Mode**: Achieved a significantly higher accuracy of **80.32%** and MCC of **0.61** .
* **Validation**: Evaluated using 5-fold cross-validation on a non-redundant dataset of 134 GTP-binding protein chains .

### Integrated Features
* **Compositional Analysis**: Includes models based on amino acid composition, dipeptide composition, and tripeptide composition .
* **Structural Context**: The method accounts for the local environment of the central residue in overlapping sequence windows.

---

## Overview of Model Development

The training dataset was derived from the PDB (Protein Data Bank), selecting 134 non-redundant protein chains with a sequence identity cut-off of 40% [cite: 1]. Interacting residues were defined as those with at least one atom within 3.5 Å of any atom of the GTP molecule [cite: 1].

| Input Feature | Accuracy | MCC | Sensitivity | Specificity |
| :--- | :--- | :--- | :--- | :--- |
| **Binary Profile** | 70.81% | 0.42 | 70.32% | 71.30% |
| **PSSM Profile** | **80.32%** | **0.61** | **80.32%** | **80.32%** |

---

## Applications

* **Signal Transduction**: Analyzing G-protein coupled receptors (GPCRs) and small GTPases like Ras .
* **Protein Synthesis**: Investigating elongation factors and initiation factors .
* **Traffic Control**: Studying Rab proteins involved in vesicle docking and fusion .

---

## Contact & Support

**Prof. G.P.S. Raghava** Head, Department of Computational Biology  
Indraprastha Institute of Information Technology (IIIT-Delhi), India.  
**Email**: raghava@iiitd.ac.in 

---

## License

This research and associated software are distributed under the **Creative Commons Attribution License (CC BY 2.0)**, allowing for unrestricted use and distribution with proper credit to the original authors [cite: 1].

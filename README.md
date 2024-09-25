# ACT5-Dataset

This README file provides an overview of the dataset used in the experiments conducted for the paper titled `ACT5 Electrical Impedance Tomography System`. The dataset contains the necessary information and resources to understand the experiments described in the paper.

## Table of Contents
- [Dataset Description](#Dataset-Description)
- [Experiments and Files](#Experiments-and-Files)
  - [ACT 5 Distinguishability Experiments](#ACT5-Distinguishability-Experiments)
  - [Frequency Experiments](#Frequency-Experiments)
  - [Adaptive Current Patterns](#Adaptive-Current-Patterns)
- [Collaborators](#Collaborators)
- [Contributing](#Contributing)
- [Contact Information](#Contact-Information)
- [Citation](#Citation)
- [Acknowledgement](#Acknowledgement)

## Dataset Description

The dataset consists of a collection of data files used in the experiments conducted for the research paper. It encompasses various datasets, input configurations, and experimental results that were utilized to analyze and validate the research findings.

## Experiments and Files
Experiments are broken down to various section, with each section regarding on aspect of capabilities of ACT 5.
These aspects include the ability of ACT 5 to detect small changes in the conductivity of the medium, ability of ACT 5 to take EIT images in various frequencies, ability of ACT 5 to apply any given current patterns, and human data collected by the ACT 5 system.

### ACT 5 Distinguishability Experiments 
Folder: `Distinguishability/`

In this set of experiments, a small target is inserted (or removed) from the center of the tank filled with saline as shown in `Distinguishability/Tragets_Tank_Middle.jpg`. The tank has a diameter of 
cm and is filled with saline with conductivity of 390 mS/m.
The metal targets have diameters 4.76 mm, 3.57 mm, 2.78 mm, and 1.59 mm as shown  in `Distinguishability/Targets_Size.jpg`.
Maximum amplitude of applied current from each source was set at 0.25 mA and the data was collected at 4 frequencies of 23 kHz, 94 kHz, 141 kHz, and 199 kHz.
For each experiment, 1500 number of frames were collected. For the three larger targets, the data collection started with the target in the saline and the target was removed during the data collection. For the smallest target, the data collection started with only saline in the tank and the target was inserted in the tank at some point during the data collection.
The data is save in `Xmm-YkHz.mat` files where `X` is the floor of the diameter of the target and `Y` is the excitation frequency.

Each data file has multiple elements: 
- `burst_frequency` is the exact value of the excitation frequency.
- `sysem_frame_rate` is the frame rate of the acqureid data. (~27 frames/sec)
- `current_patterns` is the applied current patterns in Amperes. Columns represent patterns applied simultaneously, and the rows represent current applied from one electrode at different patterns in a frame.
- `frame_voltage` is the measured frame voltage in Volts. Columns represent votlages measured simultaneously, the rows represent voltages measured from one electrode at different patterns in a frame, and the thrid dimension represent different frames of data.

---
### Frequency Experiments
Folder: `Frequency/`

The frequency experiments include opeartion of ACT 5 in a wide range of frequencies and validation of results through measurements on a saline-filled test cell using an LCR meter.

#### ACT 5 Frequency Experiments 
Folder: `Frequency/ACT5_Saline_Tank/`

To measure the behavior of ACT 5 in various frequencies, data was collected on a tank with diameter of 30 cm, once fileld with only saline and once with targets in the tank.
Top view image of the targets is shown in `Frequency/ACT5_Saline_Tank/Targets_photo/jpg`.
The data was collected at multiple frequencies, ranging from 5 kHz to 451 kHz.
Maximum applied current from each electrode was set at 200uA.
For each experiment, 500 frames of data was collected.
The data for each experiment is stored in MATLAB `.mat` files.
The data of experiments wiht only saline in the tank can be found under `Frequency/ACT5_Saline_Tank/XkHz-Empty.mat` files and the experiments with the targets in the tank are stored under the `Frequency/ACT5_Saline_Tank/XkHz-Targets.mat` name, where `X` is the frequency of the excitation signals.
Each data file has multiple elements: 
- `burst_frequency` is the exact value of the excitation frequency.
- `sysem_frame_rate` is the frame rate of the acqureid data. (~27 frames/sec)
- `current_patterns` is the applied current patterns in Amperes. Columns represent patterns applied simultaneously, and the rows represent current applied from one electrode at different patterns in a frame.
- `frame_voltage` is the measured frame voltage in Volts. Columns represent votlages measured simultaneously, the rows represent voltages measured from one electrode at different patterns in a frame, and the thrid dimension represent different frames of data.


#### LCR Meter Frequency Experiments (For Validation) 
Folder: `Frequency/LCR_Meter_Cell/`

There are four experiments of measuremens of equivalent parallel capacitance (Cp) and resistance (Rp) of a test cell in 4 configurations: 
1. `Frequency/LCR_Meter_Cell/LCR_Rp_Cp_Saline.csv` cell filled with only saline, 
2. `Frequency/LCR_Meter_Cell/LCR_Rp_Cp_PVC.csv` cell filled with saline with a PVC target in the cell
3. `Frequency/LCR_Meter_Cell/LCR_Rp_Cp_UnpolishedCopper.csv` cell filled with saline with an unpolished copper target in the cell
4. `Frequency/LCR_Meter_Cell/LCR_Rp_Cp_PolishedCopper.csv` cell filled with saline with a polished copper target in the cell.
Each file has three columns, the first column is the frequency of measurement, the second column is the parallel capacitance, and the third columns is the parallel resistance.


`cell-saline.jpg`, `cell-copper.jpg`, and `cell-PVC.jpg` are images of the experimental setup.
The measurements were done using a Sourcetronic ST2829C precision LCR meter.

---

### Adaptive Current Patterns
Folder: `Adaptive_Patterns/`

In this set of experiments, agar heart and lung targets are imaged in the tank. The setup of the experiment is shown in `Adaptive_Patterns/Agar_Targets.jpg`
Three sets of data is collected from the tank.
- `Adaptive_Patterns/Agar_Targets_Trigonometric.mat` is the experiment with trigonometric current patterns applied to the tank.
- `Adaptive_Patterns/Agar_Targets_Pair_Drive.mat` is the experiment with adjacent pair-drive current patterns applied to the tank.
- `Adaptive_Patterns/Agar_Targets_Adaptive.mat` is the experiment where the adaptive current patterns are applied to the tank.
For eac experiment, a total of 500 data frames were captured.

Each data file has multiple elements: 
- `burst_frequency` is the exact value of the excitation frequency. (99609.375 Hz in this set of experiments)
- `sysem_frame_rate` is the frame rate of the acqureid data. (~27 frames/sec)
- `current_patterns` is the applied current patterns in Amperes. Columns represent patterns applied simultaneously, and the rows represent current applied from one electrode at different patterns in a frame.
- `frame_voltage` is the measured frame voltage in Volts. Columns represent votlages measured simultaneously, the rows represent voltages measured from one electrode at different patterns in a frame, and the thrid dimension represent different frames of data.

---

## Collaborators

The data presented in this dataset was collected with the help of the following individuals.

| Name | Affiliation |
| ---- | ---- |
| Omid Rajabi Shishvan    | University at Albany    |
| Ahmed Abdelwahab    | University at Albany    |
| Nilton Barbosa da Rosa Jr.    | Colorado State University    |
| Gary J. Saulnier    | University at Albany    |
| Jennifer J. Mueller    | Colorado State University    |
| Jonathan C. Newell    | Rensselaer Polytechnic Institute    |
| David Isaacson    | Rensselaer Polytechnic Institute    |


## Contributing

As this dataset is associated with a research paper, contributions to the dataset itself may not be applicable. However, you are encouraged to provide feedback, suggestions, or report any issues related to the dataset by creating an issue in the repository.

## Contact Information

For any further inquiries or questions regarding the dataset, please contact:

- [Omid Rajabi Shishvan](mailto:orajabishishvan@albany.edu)

## Citation

If you use this dataset for your research or refer to it in any way, please cite the corresponding paper:

```
Rajabi Shishvan, Omid, Ahmed Abdelwahab, Nilton Barbosa da Rosa, Gary J. Saulnier, Jennifer L. Mueller, Jonathan C. Newell, and David Isaacson. "ACT5 Electrical Impedance Tomography System." IEEE Transactions on Biomedical Engineering (2023)
```

We appreciate your interest in our dataset and hope it proves to be a valuable resource for your research or analysis.

## Acknowledgement
  
Research reported in this dataset was supported by the National Institute of Biomedical Imaging and Bioengineering of the National Institutes of Health under award number 1R01EB026710-01A1. 
The content is solely the responsibility of the authors and does not necessarily represent the official views of the National Institutes of Health.

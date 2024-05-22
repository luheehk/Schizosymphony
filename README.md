# Schizosymphony

## Data and Data Preprocessing
The functional magnetic resonance imaging (fMRI) data from the Function Biomedical Informatics Research Network (FBIRN) dataset were processed with the [NeuroMark](https://www.sciencedirect.com/science/article/pii/S2213158220302126) pipeline. Subject-specific functional components and corresponding time courses were then estimated using the spatial constrained ICA. Four postprocessing steps were performed on the extracted time courses, including detrending, removing head motions, dispiking, and filtering with 0.15Hz low-pass filter. The FNC matrix was subsequently computed as the Pearson correlation between the paired time courses of 53 intrinsic connectivity networks (ICNs), leading to a matrix with size 53x53. These 53 ICNs were assigned to 7 functional domains including the subcortical (SC), auditory (AU), sensorimotor (SM), visual (VI), cognitive control (CC), default mode (DM) and cerebellar (CB) domains. The dynamic functional network connectivity (dFNC) data were estimated using a graphical LASSO method on the windowed data. The window width covered 20 TRs with a step size of 1 TR, resulting in 137 windows in the FBIRN dFNC data.

### Schizophrenia Subject
[dfnc_patient_001.csv](https://drive.google.com/file/d/1Hcirl9NHMlgJ_5GP0UHXdOWVQpPO4bN7/view?usp=sharing) is the dFNC data of one schizophrenia subject in CSV format. There are 1378 rows (upper triangle of 53x53 dFNC matrix) and 137 columns (time windows).

[ts_patient_001.csv](https://drive.google.com/file/d/1ZyY6ilq6DHQgv7KdOQChOpSdFhpnPFJI/view?usp=sharing) is the time series data of the 53 intrinsic connectivity networks (ICNs) in the FBIRN dataset. There are 53 rows (ICNs) and 157 columns (time points).

### Control Subject
[dfnc_control_010.csv](https://drive.google.com/file/d/1fG8bBmEnbyGExaEk64c-QHtIsHWh-pHp/view?usp=sharing) is the dFNC data of one control subject in CSV format. There are 1378 rows (upper triangle of 53x53 dFNC matrix) and 137 columns (time windows).

[ts_control_010.csv](https://drive.google.com/file/d/1JusBN5Mq77BWjXxGVQMYPJVH1Tbo-T_K/view?usp=sharing) is the time series data of the 53 intrinsic connectivity networks (ICNs) in the FBIRN dataset. There are 53 rows (ICNs) and 157 columns (time points).

## Network Information
[network_indices.txt](network_indices.txt) is a text file including the network indices of 1378 dFNC features.

[ICN_coordinates.xlsx](ICN_coordinates.xlsx) is a spreadsheet with the 3D coordinates of the intrinsic connectivity networks (ICNs) used in the dFNC analysis.

## Scripts
[load_dfnc.ipynb](load_dfnc.ipynb) is a Python script to load and visualize the dFNC data.

## Documents
[Georgia Tech S.A.W. 2024 Document](https://docs.google.com/document/d/10lzfJmFucl341rtTUpNijfQZ5F1DF2OhxqVxM9AQB9Y/edit?usp=sharing)

[OHBM 2024 BrainArt Exhibition Proposal](https://docs.google.com/document/d/1YaN2wlQmluxbHWdqqnBTnhmyaJEggCaikvZsjQ0geTE/edit?usp=sharing)

## References
[NeuroMark: An automated and adaptive ICA based pipeline to identify reproducible fMRI markers of brain disorders](https://www.sciencedirect.com/science/article/pii/S2213158220302126)

[Dynamic functional network reconfiguration underlying the pathophysiology of schizophrenia and autism spectrum disorder](https://onlinelibrary.wiley.com/doi/full/10.1002/hbm.25205)

[The Function Biomedical Informatics Research Network Data Repository](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4651841/)

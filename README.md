# Size-and-encapsulation-probability-from-DLS-data

## Overview
This project plots particle size distribution from dynamic light scattering measurments. For data on compartments (e.g. phospholipid vesicles or water droplets), estimate the probability of encapsulating a given molecule (e.g. DNA template or enzyme) within each compartment.

## Workflow

```
Raw data from DLS → Organize data into excel document → Plot data and calculate probabilities
```

1. **Raw data from DLS:** Usually .txt files from Malvern Zetasizer
2. **Organize data into excel document:** Organize each sample into its own excel worksheet. Particle size data are in the first column, subsequent columns contain replicate intensity measurments.
3. **Plot data and calculate probabilities:** Encapsulation_vs_compartment size

## Requirements

- Python 3.8+
- Required Python packages: `pandas`, `numpy`


### Input Files
- **.xlsx files:** Organize each sample into its own excel worksheet. Particle size data are in the first column, subsequent columns contain replicate intensity measurments.

## Input variables

| Parameter | Description |
|-----------|-------------|
| `filepath` | string specifying the location of excel doc containing your data |
| `samples` | list of strings corresponding to label for each sample on your excel sheet |
| `sizes_label` | string label for the column containing diameter values |
| `intensity_replicates_labels` | list of strings corresponding to label for each column containing replicate intensity measurments |
| `colors_list` | list containing strings for a color to plot each sample |
| `molecule_conc` | concentration of molecule for which you want to estimate probability of encapsulation |
| `molecule_color` | color to display the estimated probabilities |

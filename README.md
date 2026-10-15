# U.S. County-Level Patent and Technology Diffusion Analysis

This repository contains a final module assignment that studies how technological activity develops across U.S. counties using historical patent, population, business, and spatial data.

The project combines:

- **technological specialization** using county-level location quotients (LQ),
- **county technology profiles (PCA + archetypal analysis)** based on CPC 3-digit patent profiles,
- **predictive modelling**

- `f_a_bds26_v1.2.ipynb` - main notebook for Parts 1 to 3 of the analysis
- `4part_analysis.md` - Part 4 written interpretation of the infographic and business implications
- `part4_infographic.png` - visual summary used in the final discussion
- `requirements.txt` - Python dependencies
- `data/` - patent, population, county business, and shapefile inputs used by the notebook

## Analysis scope

### Part 1 - Technological specialization and county profiles

Builds county x CPC 3-digit patent profiles for the 1990-2000 study window and computes location quotients. A z-scored PCA and archetypal analysis (with and without PCA) test whether county profiles are archetypal. They form a continuum from rural-mechanical to high-tech, with small textile and chemical niches, rather than a few distinct types. Dominant archetypes are mapped, and counties are ranked as highly specialized (HHI), diversified (entropy) or technologically distinct (z-score distance).

### Part 2 - Predicting patenting activity

Uses county-level explanatory variables such as R&D employment and firm density to model patenting intensity and compare baseline and supervised machine learning approaches.

### Part 3 - Diffusion of technology across U.S. counties

Tracks the spread of **A61 medical technology** across counties over time, estimates a diffusion curve, and evaluates spatial clustering with Moran's I and local spatial indicators.

### Part 4 - Investor interpretation

Summarizes the results for a technology-investor audience, focusing on where innovation is concentrated, how specialization changes, and what the diffusion pattern implies for strategy.

## Main datasets

The repository includes the core input files directly in `data/`, including:

- historical patent files from the HistPat / USPTO-based workflow,
- county population and census/business pattern inputs,
- and U.S. county shapefiles for spatial analysis.

The notebook expects these files to remain in the existing `data/` structure.

## Python environment

The notebook was authored with **Python 3.12.1** and uses packages listed in `requirements.txt`, including:

- pandas
- numpy
- geopandas
- matplotlib
- seaborn
- scipy
- scikit-learn
- libpysal
- esda
- mapclassify
- jupyter
- ipykernel
- nbconvert

## How to run

1. Create and activate a virtual environment.
2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

   or:

   ```bash
   jupyter lab
   ```

4. Open `f_a_bds26_v1.2.ipynb` and run the cells in order.

## Outputs

Key outputs from the project include:

- county technology archetypes,
- specialization comparisons across counties,
- predictive model evaluation metrics,
- diffusion and Moran's I summaries for A61,
- maps of patent concentration and clustering,
- and the final investor-facing infographic and written interpretation.

## Notes

- The repository includes an existing local virtual environment folder (`f_venv/`), but creating your own environment is recommended for reproducibility.
- Some analyses depend on spatial libraries that may require a working scientific Python setup.
- The notebook uses relative paths, so running it from the repository root is the safest option.

# calculation-of-PEC-in-tdcs-simulation
This Project models transcranial Direct Current Stimulation (tDCS) using SimNIBS to simulate electric field distributions in various head models. It correlates simulation outcomes with clinical data to identify brain regions linked to optimal results. The project uses Python for simulation, data processing, and visualization.

## Prerequisites

- Python 3.x
- Conda
- SimNIBS
- Pandas
- Numpy
- Scipy
- Mayavi

### Setting Up SimNIBS Environment

1. **Install Conda**

   If you don't already have Conda installed, download and install it from [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution).

2. **Create and Activate Conda Environment**

   ```bash
    conda env create -f <path_to_your_downloaded_environment_file>
    conda activate simnibs_env
    pip install -f https://github.com/simnibs/simnibs/releases/latest simnibs

Use the SimNIBS documentation to install the latest SimNIBS environment file: https://simnibs.github.io/simnibs/build/html/installation/conda.html

3. **Install SimNIBS**

   ```bash
    conda install -c conda-forge simnibs

###  Project Structure

1. simulate_tdcs.py: Main script to run tDCS simulations using CSV files that contain tDCS montages with a well know order.
2. create_matrice_totale.py: Script to create the total matrix from simulation results, maintaining the same order of the tDCS montages.
3. correlate_results.py: Script to correlate simulation outcomes (electrical field) with clinical outcomes (effect size or any clinical measurement) of each tDCS montage, maintaining the same order.
4. visualize_results.py: Script to visualize PEC values on the brain mesh.
5. data/: Directory containing input CSV files and other data.
6. results/: Directory to save simulation and correlation results.

###  Usage

1. Update the file paths in the scripts to match your local environment.
2. Run the scripts in the following order:
- simulate_tdcs.py
- create_matrice_totale.py
- correlate_results.py
- visualize_results.py

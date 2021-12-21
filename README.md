# TiltedV-2D
This repo contains a setup to run ensemble simulations for 2D Tilted-V domain run with ParFlow.  The domain (illuatrated below) and the ensemble simulations are detailed in [Maxwell et al. (2021)](https://www.mdpi.com/2073-4441/13/24/3633) 

![picture 1](images/tiltedV.png) 

## Repo Contents
This repo contains python scripts to generate the baseline tilted v configuration and to run ensembles of simulations systematically altering parameters from the baseline. 
1. Baseline setup (`Baseline_tiltedV.py`): This generates the yaml script for the baseline simulation. All of the ensemble members start from this setup. Note that this script doesn't actually run ParFlow it just creates the baseline database. You must run this before running the ensembles. 
2. Ensembles (`PF_TiltedV_train_in_range.py`, `PF_TiltedV_valid_in_range.py`, `PF_TiltedV_valid_out_range.py`): These scripts run ensembles of ParFlow simulations systematically varying model parameters. In each case a directory is created for the ensemble and a subdirectory for each run. Additionally an `ensemble_settings.csv` file that records all of the settings for each run number is created in the main folder. 


**Reference**
<Br>
*Maxwell, R.M.; Condon, L.E.; Melchior, P. A Physics-Informed, Machine Learning Emulator of a 2D Surface Water Model: What Temporal Networks and Simulation-Based Inference Can Help Us Learn about Hydrologic Processes. Water 2021, 13, 3633. https://doi.org/10.3390/w13243633*

# Gammapy lectures and tutorials at Thai-CTA workshop

## Installation and set-up 

We reccomend that you install gammapy via conda

- $ curl -O https://gammapy.org/download/install/gammapy-0.18.2-environment.yml
- $ conda env create -f gammapy-0.18.2-environment.yml
- $ conda activate gammapy-0.18.2

To download the tutorials and associated datasets (necessary for the tutorials in this workshop)

- $ gammapy download tutorials
- $ cd gammapy-tutorials 
- $ export GAMMAPY_DATA=$PWD/datasets

To check if everything is working fine, open a new terminal and type

- $ conda activate gammapy-0.18.2 
- ipython

In the ipython window, type
- from gammapy.data import DataStore
- ds = DataStore.from_dir("$GAMMAPY_DATA/hess-dl3-dr1")
- [5]: obs = ds.get_observations()
- [6]: len(obs)

If the cells run without any error and prints `105`, **Congratulations! You have correctly set-up gammapy**

In case of any trouble, please contact
- Atreyee Sinha [atreyee.sinha@umontpellier.fr]
- Bruno Khelifi [khelifi@in2p3.fr>]

# Data Mining

## Slides

In this repo you can find the presentation slides from the workshop.

## Notebook

The notebook is available at [this repo](https://github.com/Lyalpha/MPAGS_Data_Mining/tree/wake).

The README in that repo contains a Binder link to launch the notebook envrionment directly in a browser.

Alternatively, the notebook can be ran locally, e.g.:

```bash
# Grab a local copy of the repository
git clone https://github.com/Lyalpha/MPAGS_Data_Mining
cd MPAGS_Data_Mining

# Check out the branch for the WAKE version and pull any updates
git checkout -b wake
git pull origin wake

# Make a virtual environment for our notebook to run under
python3 -m venv .venv
# and then activate this environment
source .venv/bin/activate
# At this point you should see `(.venv)` at the start of your terminal prompt

# Make sure our installation manager is up to date, and then install the required packages into our environment
pip install --upgrade pip
# If you are on python version >=3.7, <3.10, then run:
pip install -r requirements.txt 
# OR if you are python version >=3.10, then run:
pip install -r requirements-py3.10.txt 


# Install jupyter lab so we can launch the notebook
pip install jupyterlab

# finally, launch the lab to run the notebook
jupyter-lab
```

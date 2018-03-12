# Perturb-and-MAP approach for learning Restricted Boltzmann Machines

This repository contains code for the Perturb-and-MAP learning for Restricted Boltzmann Machines with Caffe backend and Python runtime.

# Usage 

- Clone repository with both submodules with: 
```bash
git clone --recurse-submodules https://github.com/szymonzareba/perturb_and_map_rbm.git
```

- `perturb_and_map_caffe` code needs to be compiled using `Makefile`. Please refer to the example configuration in `Makefile.config.example` and my current configuration in `Makefile.config`
- Python wrappers in `perturb_and_map_caffe/python` need to be added to `PYTHONPATH` to be available in Python code
- `perturb_and_map_python` contains runtime for compiled Caffe code:
    - `datasets` contains datasets to be used in training, please not that due to size limit, not every file is included in repository and you may need to prepare some data. `20Newsgroup`, `omniglot` and `toy` dataset are complete
    - `inits` contains text files with initial weights to be used in training
    - `run_all.py` runs training for all defined experiments
    - `eval.py` contains various methods used in metric calculation, visualizations etc.

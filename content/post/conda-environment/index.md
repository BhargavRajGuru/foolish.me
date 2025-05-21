---
title: 💾 Set up conda environment
summary: There's lots to learn!
date: 2023-08-03

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Conda**](https://docs.conda.io)'

authors:
  - admin

tags:
  - Academic
  - Wowchemy
  - Markdown
---

# Anaconda cheat sheet

## conda environments

This is a simple cheat sheet to set up and start using conda environment

To see all installed packages

```bash
conda list
```

To create new enviroment with name myenv

```bash
conda create --name myenv
```

To create new environment specifying the packages to be installed

```bash
conda create --name env python=3.7 numpy=1.18 pyserial
```

This is to create enviroment at different path, first go to that path and use the command below

```bash
conda create -p ./myenv
```

This command does the same thing as above

```bash
conda create --prefix ./myenv
```

To activate the environment

```bash
conda activate D:\pythoncode\myenv
```

if you're at the directory of environment

```bash
conda activate ./myenv
```

To install python with a particular version in conda environment

```bash
conda install python=3.7
```

Install several packages together
```bash
conda install numpy pyserial pyyaml pyqt pyqtgraph
```

I need to read about this command

```bash
conda install -c conda-forge pint
```

To deactivate conda environment

```bash
conda deactivate
```

To exit from the conda environment

```bash
exit()
```

To remove the conda environment

```bash
conda remove --name env --all
```

To remove the conda environment at different path

```bash
conda env remove -p D:\pythoncode\envqiskit-metal
```

Creating an environment from an environment.yml file

```bash
conda env create -f environmet.yml
```

Export your active environment to a new file

```bash
conda env export > environment.yml
```

## That's all
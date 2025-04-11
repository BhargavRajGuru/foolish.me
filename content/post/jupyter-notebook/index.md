---
title: Jupyter Notebook inside your Conda environment
summary: How you choose to interact with your kernels in Jupyter Notebook!
date: 2025-04-11

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: Image created by Scriberia for The Turing Way community (CC-BY license)'

authors:
  - admin

tags:
  - Academic
  - Wowchemy
  - Markdown
---

This method doesn't actually get your environment to show in Jupyter Notebooks, but it is worth trying. If you install jupyter in any environment and run jupyter notebook from that environment the notebook will use the kernel from active environment. The kenel will show with the default name Python 3 but we can verify this works by doing the following.

1. Activate your environment, install jupyter, and run jupyter notebook.

Ignore this step if you have already created a conda environment.

```bash
(base)$ create -p ./new-env
```

```bash
(base)$ conda activate D:\pythoncode\new-env
```

```bash
(D:\pythoncode\new-env)$ conda install jupyter
```

```bash
(D:\pythoncode\new-env)$ jupyter notebook
```

{:start="2"}
2. Run the following code in your notebook to confirm that you are using the correct kernel.

```python
import os
print (os.environ['CONDA_DEFAULT_ENV'])
```
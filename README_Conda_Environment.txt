This file details the Installation instructions for the conda environment used in this project. Also,  details for removing or maintaining are present. 
After installation, open Jupyter notebook by typing Jupyter notebook in the command shell. Next, go through the different notebooks to install the code.

### 🧰 Prerequisites

Make sure you have **[Miniconda](https://docs.conda.io/en/latest/miniconda.html)** or **[Anaconda](https://www.anaconda.com/download)** installed.

Check your Conda installation:
```anaconda prompt
conda --version
```

---

### ⚙️ Create the Environment

In the project directory (where `environment.yml` is located), run:
```anaconda prompt
conda env create -f environment.yml
```

This will:
- Create a new environment with the name specified in the `.yml` file.
- Install all listed dependencies (Python version, libraries, etc.).

---

### 🚀 Activate the Environment

Once created, activate it with:
```anaconda prompt
conda activate <environment_name>
```

To check the environment name, look at the first line in `environment.yml`, e.g.:
```yaml
name: myproject
```

---

### 🔄 Updating the Environment

If you modify the `environment.yml` (e.g., add a new dependency):
```anaconda prompt
conda env update -f environment.yml --prune
```
The `--prune` option removes old packages that are no longer needed.

---

### ❌ Removing the Environment

If you need to delete it:
```anaconda prompt
conda env remove -n <environment_name>
```

---

### 📦 Exporting a Fresh Environment

If you install new packages and want to update the file:
```anaconda prompt
conda env export --no-builds > environment.yml
```

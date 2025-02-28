# intellihack5

## Python Project Setup Guide

This guide will help you set up a virtual environment for your Python project using either Conda or venv, and install dependencies from a `requirements.txt` file.

### Cloning the Repository

First, clone the repository:

```bash
git clone https://github.com/Standord-AI/intellihack5.git
cd intellihack5
```

### Setting Up a Virtual Environment

## Option 1: Using Conda

**Create a Conda environment**

You can create the environment in two ways:

*Project-specific environment (recommended):*

```bash
conda create --prefix ./conda_env python=3.10
```

*Named environment (stored in Conda's central directory):*

```bash
conda create --name project_name python=3.10
```

**Activate the environment**

For project-specific environment:

```bash
conda activate ./conda_env
```

For named environment:

```bash
conda activate project_name
```

## Option 2: Using venv

**Create a virtual environment**

```bash
# On macOS/Linux
python3 -m venv .venv

# On Windows
python -m venv .venv
```

**Activate the environment**

```bash
# On macOS/Linux
source .venv/bin/activate

# On Windows
.\.venv\Scripts\activate
```

## Installing Dependencies from `requirements.txt`

**Creating a `requirements.txt` file**

If you already have packages installed in your environment and want to create a `requirements.txt` file:

```bash
pip freeze > requirements.txt
```

**Installing packages from `requirements.txt`**

Using pip (works with both Conda and venv):

```bash
pip install -r requirements.txt
```

Using Conda (Conda environments only):

```bash
conda install --file requirements.txt
```

### Project Structure

A basic project structure might look like this:

```text
intellihack5/
├── .venv/ or conda_env/     # Virtual environment folder
├── ipynb/                   # Source files
├── README.md                # Project documentation
├── requirements.txt         # Dependencies
└── .gitignore               # Git ignore file
```

### Deactivating the Environment

When you're done working on your project:

```bash
# For both Conda and venv
conda deactivate  # For Conda
deactivate        # For venv
```

### Additional Tips

- Add your virtual environment folder to `.gitignore` to avoid committing it to version control.
- Consider using a `setup.py` or `pyproject.toml` file for more complex projects.
- For collaborative projects, ensure everyone uses the same Python version.

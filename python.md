# Python Virtual Environment Guide

This guide provides a step-by-step process for creating, using, and closing a Python virtual environment.

## Prerequisites
- Ensure Python is installed on your system.
- Verify Python installation by running:

```bash
python --version
```

## Steps to Create and Use a Virtual Environment

### 1. Create a Virtual Environment
To create a virtual environment, use the following command:

```bash
python -m venv myenv
```


This will create a folder named `myenv` in your current directory.

### 2. Activate the Virtual Environment

#### On Windows:

```bash
myenv\Scripts\activate
```

#### On macOS/Linux:

```bash
source myenv/bin/activate
```


Once activated, you will see the environment name prefixed in your terminal prompt (e.g., `(myenv)`).

### 3. Install Dependencies
You can now install packages within the virtual environment using `pip`:

```bash
pip install <package-name>
```

For example, to install `requests`:

```bash
pip install requests
```

### 4. Deactivate the Virtual Environment
To exit the virtual environment, run:

```bash
deactivate
```

Once deactivated, your terminal will return to the global Python environment.

### 5. Remove the Virtual Environment (Optional)
If you want to delete the virtual environment, simply remove the `myenv` folder:

#### On Windows:

```bash
rmdir /s /q myenv
```

#### On macOS/Linux:

```bash
rm -rf myenv
```

## Additional Notes
- Use `pip freeze > requirements.txt` to save the current environment's dependencies.
- Use `pip install -r requirements.txt` to install dependencies from a file.

This guide ensures you can effectively manage Python virtual environments for your projects.
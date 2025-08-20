# Physical_Climate_Science_Course
Repository for GEOS 5300 Physical Climate Science at the University of Texas at Dallas

## Setup Instructions

## Step 1. Install Miniconda

Anaconda is a popular distribution of Python for data science that simplifies package management. **Miniconda** is a lightweight version of Anaconda. It includes only the essentials: Python, the `conda` package manager, and a few basic packages. You will use `conda` to install and manage Python packages and environments for this class.  

👉 If you already have **Anaconda** or **Miniconda** installed on your computer (e.g., from another class), you can **skip this step** and go to **Step 2**.

---

### For macOS users
1. Check which processor your Mac has:
   - Click the **Apple icon** in the top-left corner → **About This Mac**.  
   - Note whether it says **Intel** or **Apple M1/M2 (Apple Silicon)**.  
   You’ll need this information to choose the correct installer.  

---

### Download and Install
1. Go to the official Miniconda installation page:  
   [Miniconda Installation Guide](https://www.anaconda.com/docs/getting-started/miniconda/install)  

2. Under **Basic install instructions**, choose your operating system (**Windows** or **macOS/Linux**).  

3. Download the **64-Bit Graphical Installer** that matches your operating system (and processor type if you are on a Mac).  

4. Run the installer:  
   - Agree to the license terms.  
   - Use the **default installation location** suggested by the installer.  
   - Click **Install** (this may take a few minutes).  

5. Once the installation finishes, click **Next**, then **Finish**.  

---

### Verify Installation
1. Open a new **terminal** (on macOS/Linux) or **Anaconda Prompt** (on Windows).  
2. Type:  
   ```bash
   conda

## Step 2. Set Up Your Physical Climate Science Course Environment

**1. Create a new folder for this course. ** 
   For example, I created a folder named 'Phy_Clim_Sci_Course' under /Users/xianwu/Documents/python/teaching/ on my Mac.

**2. Navigate to this directory. For example, on macOS:**
```
cd /Users/yourusername/Documents/EV333_AtmosphericScience
```
**3. Add conda-forge Channel**
```
conda config --add channels conda-forge
```
**4. Create a New Python Environment**
```
# Create environment with core packages only, let conda resolve dependencies
conda create -n PhyClimSci -c conda-forge python=3.11 jupyterlab xarray netcdf4 matplotlib numpy cartopy pandas h5netcdf xesmf cmocean scipy

```

**5. Activate your Environment**
```
conda activate PhyClimSci
```
# Install Cartopy and PyProj after environment is created
```
conda install -c conda-forge cartopy=0.23.0 pyproj geos proj libtiff
```

Check your Python version
```
python --version
```
List environments:
```
conda env list
```
(Not now) In the future, if you need to install additional packages:
```
# Install NetCDF4 (specific version)
pip install netCDF4==1.6.2

# Reinstall dask
conda install dask --force-reinstall

# Check installed packages
conda list
```
## Step 3. Launch Jupyter Lab
#enter the course directory
```
cd /Users/yourusername/Documents/EV333_AtmosphericScience

#launch Jupyter lab
jupyter lab
```
**Download the first notebook,** `PhyClimSci_Lecture1_Introduction_SAT_Rainfall.ipynb`, from this GitHub repository. Save it in your course directory and rename it by appending your name. For example: `PhyClimSci_Lecture1_Introduction_SAT_Rainfall_Xian_Wu.ipynb`.
 
   
Run the cells by clicking the play button. Hope this will work for you!


## License

- Code in this repository is licensed under the [MIT License](./LICENSE).
- Written instructional content and figures are licensed under
  [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).

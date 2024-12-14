# SWAG_COUPLED_MODEL 
## Urban Flooding Coupled Simulation System

**A powerful coupled simulation system for modeling urban surface-drainage network flooding processes, based on ANUGA and SWMM. This system allows integrated simulation of surface flooding and drainage network flows.**

---

## 🚀 **Key Features**

### 1. **Surface Flood Simulation (ANUGA)**
- **Multi-resolution mesh generation**
- **DEM-based terrain modeling**
- **Water depth and velocity output**
- **Results export to DEM and Shapefile formats**

### 2. **Drainage Network Simulation (SWMM)**
- **Node and pipe network modeling**
- **Overflow process simulation**
- **Detailed simulation reporting**
- **Multiple hydraulic model options**

### 3. **Coupling Capabilities**
- **Integration** of drainage overflow points with surface model
- **Result format conversion**
- **Time series data exchange**

---

## 📁 **File Structure and Descriptions**

### `/SWAG_COUPLED_MODEL`
- **`Bantian_simulation.ipynb`**: Main ANUGA simulation program
  - Mesh generation and configuration
  - DEM data import
  - Boundary condition setup
  - Simulation execution and visualization
  - Results export functionality

- **`extract_information_from_swmm.ipynb`**: SWMM data processing program
  - Node name batch modification
  - Overflow statistics calculation
  - Result format conversion for coupling
  - Time series data extraction

- **`swmm_folder/`**: SWMM related files
  - **`swmm.inp`**: SWMM input file
    - Network structure definition
    - Simulation parameters
    - Rainfall data
  - **`swmm.rpt`**: SWMM report file
    - Simulation results
    - Error messages
    - Performance statistics
  - **`swmm.ini`**: SWMM configuration file
    - Display settings
    - Map options
    - Default values

- **`shp/`**: Spatial data folder
- **`output_shapefile.cpg`**: Character encoding file
- **`add_buildings.cpg`**: Building data encoding file

---

## 🛠 **Usage Instructions**

### **1. ANUGA Simulation**
1. Configure simulation parameters in `Bantian_simulation.ipynb`
2. Import required terrain and boundary data
3. Run the simulation and export results
4. Convert results to required formats

### **2. SWMM Simulation**
1. Process SWMM data using `extract_information_from_swmm.ipynb`
2. Modify node names if needed
3. Calculate overflow statistics
4. Convert results for coupling with ANUGA

---

## ⚙️ **Technical Requirements**

- **Python 3.9+**
- **ANUGA Hydraulic Modeling Package**
- **PySWMM**
- **netCDF4**
- **numpy**
- **matplotlib**
- **geopandas**

---

## 🗺 **Data Requirements**

### **1. Terrain Data**
- DEM files
- Building footprints
- Boundary polygons

### **2. Drainage Network Data**
- Node locations
- Pipe network layout
- Network parameters

---

## ⚠️ **Important Notes**

### 1. **Environment Setup**
- Ensure all dependencies are correctly installed
- Verify Python version compatibility
- Check ANUGA and SWMM installations

### 2. **Data Preparation**
- Verify data file paths
- Check coordinate systems
- Validate input data formats

### 3. **Simulation**
- Calibrate model parameters
- Verify boundary conditions
- Monitor simulation stability

### 4. **Results**
- Backup simulation results
- Validate output formats
- Check coupling consistency

---

## ❗️ **Known Limitations**
1. Large-scale simulations may require significant computational resources
2. The coupling process may need manual intervention
3. Result accuracy depends on input data quality

---

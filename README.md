# Caravel User Project

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0) [![UPRJ_CI](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/user_project_ci.yml) [![Caravel Build](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml/badge.svg)](https://github.com/efabless/caravel_project_example/actions/workflows/caravel_build.yml)

| :exclamation: Important Note            |
|-----------------------------------------|

## Please fill in your project documentation in this README.md file 

Refer to [README](docs/source/index.rst#section-quickstart) for a quickstart of how to use caravel_user_project

Refer to [README](docs/source/index.rst) for this sample project documentation. 

Refer to the following [readthedocs](https://caravel-sim-infrastructure.readthedocs.io/en/latest/index.html) for how to add cocotb tests to your project. 

<details>
  <summary>Steps for installing the flow </summary>


---

### Overview
This repository contains the RV32I ASIC design project implemented using the efabless open-source framework on the Caravel user project platform. The goal is to design a RISC-V based 32-bit processor and prepare it for fabrication using the OpenLANE ASIC flow.

### Prerequisites
Before you begin, ensure you have the following installed on your Ubuntu system:
- Docker
- Python 3
- build-essential (gcc compiler, make, etc.)
- git
- Click (Python library)

You can install these prerequisites using the following commands:
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt install -y build-essential python3 python3-venv make git
sudo apt-get install docker.io
pip install click
```

### Repository Setup
1. **Clone the Project Repository:**
   ```bash
   git clone https://github.com/navi2311/rv32i.git
   cd rv32i
   ```

2. **Create ASIC Directories:**
   ```bash
   mkdir -p ~/asic/{openlane,pdk}
   ```

3. **Set Environment Variables:**
   Add the following lines to your `~/.bashrc` or `~/.profile` file to ensure these variables are set up every time you open a terminal:
   ```bash
   export OPENLANE_ROOT=~/asic/openlane
   export PDK_ROOT=~/asic/pdk
   ```
   After adding them, source the file to update your current session:
   ```bash
   source ~/.bashrc  # or source ~/.profile
   ```

### Project Configuration
1. **Initialize the Project:**
   Run the following command in the project directory to set up the environment by going into the project directory :
   ```bash
   make setup
   ```

2. **Run the ASIC Flow:**
   Navigate to the OpenLANE directory within your project and start the ASIC synthesis and layout generation:
   ```bash
   cd openlane
   make user_proj_example
   ```
   This command runs the OpenLANE flow and generates the GDSII file, which is used for fabrication.

### Additional Information
- **efabless Platform:** You can find more about efabless and Caravel user project [here](https://efabless.com).
- **User Project Template:** A template for starting a new user project on Caravel can be found [here](https://github.com/efabless/caravel_user_project).


---

</details>

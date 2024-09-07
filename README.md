# Magnetism Lab Analysis

This repository contains the scripts, data, and analysis for a magnetism laboratory experiment conducted to calculate the magnetic permeability of various ferrite materials using toroidal coils. The experiment measures inductance as a function of coil turns and applies fundamental electromagnetic principles to determine the relative permeability of different materials.

## Table of Contents

1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Usage](#usage)
    - [Steps to Run Analysis](#steps-to-run-analysis)
4. [Data and Analysis](#data-and-analysis)
5. [Equations](#equations)
6. [Contributing](#contributing)
7. [License](#license)

## Introduction

In this laboratory experiment, we aim to determine the magnetic permeability (\(\mu\)) of various ferrite materials by measuring the inductance (\(L\)) of coils wound around ferrite toroids. Inductors store energy in the form of a magnetic field and resist changes in current, making them essential components in electrical circuits. By analyzing the inductance as a function of the number of coil turns and applying electromagnetic laws, we can calculate the relative permeability (\(\mu_r\)) of the materials, classifying them as either soft or hard magnets.

## Installation

To set up the environment for running the analysis, follow these steps:

1. **Clone the Repository**
    ```bash
    git clone https://github.com/smahala02/Magnetism-Lab.git
    cd Magnetism-Lab
    ```

2. **Install Anaconda**
    - Download and install Anaconda from [here](https://www.anaconda.com/products/distribution).
    - Follow the installation instructions for your operating system.

3. **Install Dependencies**
    Ensure you have the necessary Python packages installed. You can install them using the provided `requirements.txt` file.
    ```bash
    pip install -r requirements.txt
    ```

## Usage

This section outlines how to run the analysis scripts to process the experimental data and calculate the magnetic permeability.

### Steps to Run Analysis

1. **Prepare Data Files**
    - Ensure all `.csv` data files from the experiment are placed in the `data/` directory. These files contain measurements of voltage across the resistor and the total circuit voltage for different toroids and coil turns.

2. **Open Jupyter Notebook**
    - Launch Anaconda Navigator and open Jupyter Notebook, or use the terminal:
      ```bash
      jupyter notebook
      ```

3. **Open the Analysis Script**
    - Navigate to the `scripts/` directory and open `Magnetism_script.ipynb`.

4. **Configure the Script**
    - In the notebook, specify the filename of the data you wish to analyze, the frequency used during the experiment, and the sense resistance value.

5. **Run the Analysis**
    - Execute each cell in the notebook sequentially to process the data, calculate inductance, and determine relative permeability.
    - The results, including inductance values and permeability calculations, will be displayed and saved in the `results/` directory.

6. **Review Plots**
    - Inductance vs. \(N^2\) plots for each toroid are generated to visualize the relationship and derive the slope used in permeability calculations. These plots are saved in the `plots/` directory.

## Data and Analysis

The experiment involved measuring the inductance of toroidal coils with varying numbers of turns and frequencies. The key steps in the data analysis process include:

1. **Calculating Current and Inductance**
    - The current (\(I\)) through the circuit is calculated using Ohm's law:
      \[
      I = \frac{V_R}{R}
      \]
    - The voltage across the inductor (\(V_L\)) is determined by:
      \[
      V_T = V_R + V_L
      \]
    - Inductance (\(L\)) is calculated using the impedance (\(Z_L\)):
      \[
      L = \frac{Z_L}{2\pi f}
      \]
      where \(f\) is the frequency of the AC signal.

2. **Determining Relative Permeability**
    - By plotting \(L\) against \(N^2\) (where \(N\) is the number of turns), the slope of the linear fit is used to calculate the relative permeability (\(\mu_r\)) using the formula:
      \[
      \mu_r = \frac{L \times l}{\mu_0 \times A \times N^2}
      \]
      where:
      - \(L\) = Inductance (H)
      - \(l\) = Circumference of the toroid (m)
      - \(A\) = Cross-sectional area of the toroid (m²)
      - \(\mu_0 = 4\pi \times 10^{-7} \, \text{H/m}\) (permeability of free space)

3. **Classification of Materials**
    - Based on the calculated \(\mu_r\), materials are classified as:
      - **Soft Magnets**: High relative permeability, easily magnetized and demagnetized.
      - **Hard Magnets**: Lower relative permeability, retain magnetization.

### Data Structure

- **data/**: Contains all `.csv` files with experimental measurements.
- **scripts/**: Python scripts and Jupyter notebooks for data analysis.
- **plots/**: Generated plots from the analysis.
- **results/**: Tables and calculated results from the experiments.

## Equations

The following fundamental equations were used in the analysis:

1. **Ohm's Law for Current Calculation**
   \[
   I = \frac{V_R}{R}
   \]
   - \(I\): Current (A)
   - \(V_R\): Voltage across the resistor (V)
   - \(R\): Resistance (Ω)

2. **Voltage Across Inductor**
   \[
   V_T = V_R + V_L
   \]
   - \(V_T\): Total circuit voltage (V)
   - \(V_L\): Voltage across the inductor (V)

3. **Inductance Calculation**
   \[
   L = \frac{Z_L}{2\pi f}
   \]
   - \(L\): Inductance (H)
   - \(Z_L\): Impedance of the inductor (Ω)
   - \(f\): Frequency (Hz)

4. **Relative Permeability Calculation**
   \[
   \mu_r = \frac{L \times l}{\mu_0 \times A \times N^2}
   \]
   - \(L\): Inductance (H)
   - \(l\): Circumference of the toroid (m)
   - \(A\): Cross-sectional area (m²)
   - \(N\): Number of turns
   - \(\mu_0\): Permeability of free space (\(4\pi \times 10^{-7} \, \text{H/m}\))

## Contributing

Contributions are welcome! To contribute to this project, please follow these steps:

1. **Fork the Repository**
    - Click the "Fork" button at the top right of this repository's page.

2. **Clone Your Fork**
    ```bash
    git clone https://github.com/smahala02/Magnetism-Lab.git
    cd Magnetism-Lab
    ```

3. **Create a New Branch**
    ```bash
    git checkout -b feature/your-feature
    ```

4. **Make Your Changes**
    - Implement your feature or fix.

5. **Commit Your Changes**
    ```bash
    git commit -m "Add your feature"
    ```

6. **Push to Your Fork**
    ```bash
    git push origin feature/your-feature
    ```

7. **Open a Pull Request**
    - Navigate to your fork on GitHub and click "New pull request."

Please ensure your contributions adhere to the project's coding standards and include appropriate documentation.

## License

This project is licensed under the [MIT License](LICENSE).

---

## Additional Information

### Questions

1. **What is Relative Permeability?**
    - Relative permeability (\(\mu_r\)) is a measure of how easily a material can become magnetized compared to free space. It is a dimensionless quantity indicating the efficiency of a material in enhancing the magnetic field.

2. **How is Inductance Related to Magnetic Permeability?**
    - Inductance (\(L\)) is directly proportional to the magnetic permeability (\(\mu\)) of the core material. Higher permeability materials result in higher inductance for the same coil configuration, indicating a stronger ability to store magnetic energy.

3. **Why Use Toroidal Coils?**
    - Toroidal coils provide a closed-loop magnetic path, minimizing energy loss and external magnetic field interference. This makes them ideal for precise inductance measurements and applications like transformers and inductors.

### Acknowledgements

- [All About Circuits](http://www.allaboutcircuits.com/textbook/direct-current/chpt-15/magnetic-fields-and-inductance/)
- Educational resources and laboratory equipment used in the Magnetism Lab Script.

## Author
- [smahala02](https://github.com/smahala02)



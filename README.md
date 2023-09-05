# particleShield

particleShield is a Python library designed to facilitate radiation shielding calculations. It provides a set of functions and utilities to determine the amount of radiation absorbed by different shielding materials for different types of radiation.

## Features

This Python code provides a set of functions to perform various calculations related to radiation physics, including:

- Half-value layer (HVL) calculation
- Buildup factor calculation
- Dose rate calculation
- Radiation attenuation calculation
- Bethe-Bloch equation for energy loss
- Bragg curve generation

## Requirements

- Python 3.7
- NumPy
- Matplotlib

## Installation

1. Make sure you have Python 3.7 installed on your system.

2. Install the required dependencies by running the following command:

   ```shell
   pip numpy as np, matplotlib.pyplot as plt
   ```
   
3. Download the particleShield library and import it in your project.


## Usage

The package can then be imported using:

```python
import particleShield
```
### Ionizing Radiation
particleShield provides multiple functions for calculation of radiation protection and dosimetry for different types of ionizing radiation.

```python
#Calculate the half-value layer
hvl = particleShield.calculate_hvl(initial_intensity, attenuation_factor)

#Calculate the buildup factor
buildup_factor = particleShield.calculate_buildup_factor(penetration_depth, attenuation_factor)

#Calculate the dose rate
dose_rate = particleShield.calculate_dose_rate(intensity, conversion_factor, time, distance)

#Calculate radiation attenuation
attenuated_intensity = particleShield.calculate_attenuation(I0, mu, x)
```
### Beth-Bloch equation
The Bethe-Bloch equation is used to calculate the energy loss of charged particles (e.g., electrons, protons, alpha particles) as they pass through a material. It describes how these particles lose energy through ionization and excitation of atoms in the material.

The Beth-Bloch equation:
<!-- Adjust the image size and format -->
![](https://github.com/ypragyan/ParticleShield/blob/main/bethbloch.png)




```python
#Calculate energy loss using the Bethe-Bloch equation for Protons in Air
kinetic_energy = 100  # MeV
charge = 1  # Elementary charge units
atomic_mass = 28.09  # g/mol
atomic_number = 14
ionization_potential = 78  # eV

energy_loss = bethe_bloch(kinetic_energy, charge, atomic_mass, atomic_number, ionization_potential)
print("Energy Loss:", energy_loss, "MeV/cm")
```
Output: Energy Loss: -4.297 MeV/cm

### Bragg Curve
The Bragg curve is a graphical representation that illustrates how the energy deposition of charged particles varies with depth as they traverse a material.

```python
#Generate the Bragg curve for protons in air
alpha = 0.1666  # MeV/(g/cm^2)
p = 1.76        # g/cm^2
shallowest_depth = 10.0  # cm
deepest_depth = 15.0     # cm

generate_bragg_curve(alpha, p, shallowest_depth, deepest_depth)

```
Bragg curve for protons in air:

<div style="text-align:center;">
  <img src="https://github.com/ypragyan/ParticleShield/blob/main/brag.curve" alt="Bragg Curve" width="500" height="400" style="border:1px solid black; padding:10px;">
</div>

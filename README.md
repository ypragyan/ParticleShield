# ParticleShield

ParticleShield is a Python library designed to facilitate radiation shielding calculations. It provides a set of functions and utilities to determine the amount of radiation absorbed by different shielding materials for different types of radiation.

## Features

This Python code provides a set of functions to perform various calculations related to radiation physics, including:

- Half-value layer (HVL) calculation
- Buildup factor calculation
- Dose rate calculation
- Bethe-Bloch equation for energy loss
- Bragg curve generation for protons in air
- Radiation attenuation calculation

## Requirements

- Python 3.x
- NumPy
- Matplotlib

## Installation

1. Make sure you have Python 3.x installed on your system.

2. Install the required dependencies by running the following command:

   ```shell
   pip install math, numpy as np, matplotlib.pyplot as plt
   
3. Download the ParticleShield library and add it to your project.


## Usage
To use the ParticleShield library, import the necessary functions and utilities in your Python code. Here's an example:
```python
import particleshield

#Calculate the half-value layer
hvl = particleshield.calculate_hvl(initial_intensity, attenuation_factor)

#Calculate the buildup factor
B = particleshield.calculate_buildup_factor(penetration_depth, attenuation_factor)

#Calculate the dose rate
dose_rate = particleshield.calculate_dose_rate(intensity, conversion_factor, time, distance)

#Calculate energy loss using the Bethe-Bloch equation
energy_loss = particleshield.bethe_bloch(energy, z, A, Z, I)

#Generate the Bragg curve for protons in air
particleshield.generate_bragg_curve(alpha, p, shallowest_depth, deepest_depth)

#Calculate radiation attenuation
attenuated_intensity = particleshield.calculate_attenuation(I0, mu, x)
```

##License
This code is released under the MIT License. See LICENSE for details.

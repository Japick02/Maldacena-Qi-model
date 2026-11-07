# Maldacena-Qi model

In this project I developed a numerical solver for the large-N Schwinger-Dyson equations of SYK and Maldacena-Qi models. The latter is obtained with two SYK models interacting. 

I used the solvers to compute the large-N Free energy through saddle-point solutions as a function of the temperature.

All the code is based on GPU acceleration achieved through CuPy library and it has been tested on Nvidia RTX 5070.

## Notebooks

### 1. SYK SD solver and Free Energy computation

**File:** [SYK_SD.ipynb](SYK_SD.ipynb)

Numerical solver for large-N Schwinger-Dyson equations of SYK model.

<p align="center">
  <img src="figures/Green_bJ10_SYK.png" width="48%" alt="Green_bJ10">
  <img src="figures/Green_bJ50_SYK.png" width="48%" alt="Green_bJ50">
</p>


Computation of Free Energy as a function of the temperature.

<p align="center">
  <img src="figures/" width="60%" alt="SYK_SFF">
</p>

**References:** 

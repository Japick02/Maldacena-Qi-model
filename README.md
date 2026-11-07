# Maldacena-Qi model

In this project I developed a numerical solver for the large-N Schwinger-Dyson equations at finite temperature of SYK and Maldacena-Qi models. The latter consists of two coupled SYK systems. Such solver is based on an iterative method. It makes use of Fast Fourier Transform and numerical techniques to deal with Gibbs problem and aliasing, arising from non-linearity of the equations.

I used the solvers to compute the large-N Free energy through saddle-point solutions as a function of the temperature. For what concerns MQ model, I simulated the cooling and a successive reheating of the system to reproduce the hysteresis cycle.  

All the code is based on GPU acceleration, achieved using the CuPy library and it has been tested on NVIDIA RTX 5070.

## Notebooks

### 1. SYK SD solver and Free Energy computation

**File:** [SYK_SD.ipynb](SYK_SD.ipynb)

Numerical solver for large-N Schwinger-Dyson equations of SYK model.

<p align="center">
  <img src="figures/Green_bJ10_SYK.png" width="48%" alt="Green_bJ10">
  <img src="figures/Green_bJ50_SYK.png" width="48%" alt="Green_bJ50">
</p>

**File:** [Free_energy_SYK.ipynb](Free_energy_SYK.ipynb)

Computation of Free Energy as a function of the temperature.

<p align="center">
  <img src="figures/Free_energy_SYK.png" width="60%" alt="Free_energy_SYK">
</p>

**References:** J. Maldacena, D. Stanford. *Comments on the Sachdev-Ye-Kitaev model* (2016): [arXiv:1604.07818](https://arxiv.org/abs/1604.07818)

### 2. MQ SD solver and Free Energy computation
**File:** [MQ_SD.ipynb](MQ_SD.ipynb)

Numerical solver for large-N Schwinger-Dyson equations of MQ model. This is based on the SYK one.

<p align="center">
  <img src="figures/Green_high_temp_MQ.png" width="48%" alt="Green_high_temp_MQ">
  <img src="figures/Green_low_temp_MQ.png" width="48%" alt="Green_low_temp_MQ">
</p>

**File:** [Free_energy_MQ.ipynb](Free_energy_MQ.ipynb)

Computation of Free Energy as a function of the temperature and characterization of first order phase transition between two-black-holes phase and wormhole phase. I used the solution at each step to find a conformal guess to initialize the iterative algorithm for the next one.

<p align="center">
  <img src="figures/Hysteresis_conf.png" width="60%" alt="Hysteresis_conf">
</p>

I used the notebook to collect data points and plot the Phase Diagram in $\mu - T$ plane.

<table>
  <tr>
    <td width="60%">
      <img src="figures/Phase_diagram.png" width="100%" alt="Phase_diagram">
    </td>
    <td width="40%">
      <p>
       Black solid lines denote the coexistence region. Pink line denotes the critical temperature. 
      </p>
    </td>
  </tr>
</table>

**References:** J. Maldacena, X.-L. Qi. *Eternal traversable wormhole* (2018): [arXiv:1804.00491](https://arxiv.org/abs/1804.00491)

## Dependencies
Python, NumPy, CuPy, Matplotlib



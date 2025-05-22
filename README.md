# Estimating Ionic Strength from AFM Force Curves  
### Master's Degree in Quantitative Biology  
**University of Milan**  
**This Analysis has been done as a part of the course "Measurement of nanoscale interactions in biological systems and data analysis"**


---

## Project Overview

This data analysis project aims to estimate the **ionic strength (I)** of an electrolyte solution using **atomic force microscopy (AFM)** measurements of electrostatic double-layer interactions.

By fitting experimental **force–distance curves** to a physical model (DLVO theory), we extract the **Debye length (λ_D)** and compute ionic strength based on the known relationship:

$$
\lambda_D = \frac{0.304}{\sqrt{I}}
$$

---

## Method Summary

- Experimental data: `distance (nm)`, `force (nN)`, `force error (nN)`
- Model:
- 
F(d) = F₀ + a·d + c·exp(-d / λ_D)

- Fitting strategy:
  - Estimate initial parameters from linear and exponential regions
  - Perform **weighted nonlinear least squares** fit using `scipy.optimize.curve_fit`
  - Plot residuals to assess model accuracy
  - Propagate uncertainty to compute error in ionic strength


---

## Requirements

- Python 3.x  
- NumPy, Pandas, Matplotlib, SciPy  
- Jupyter Notebook

---


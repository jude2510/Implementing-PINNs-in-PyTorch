# Implementing Physics-Informed Neural Networks (PINNs) with PyTorch

This repository contains code and explanations for implementing Physics-Informed Neural Networks (PINNs) using PyTorch, reproducing key results from the foundational work of Raissi et al. (2019). PINNs offer a novel framework for solving partial differential equations (PDEs) by incorporating physical laws directly into the training loss function of deep neural networks.

📄 [Project Report (PDF)](./Project%20Report.pdf)

---

## 🧠 Overview

Physics-Informed Neural Networks (PINNs) are deep learning models designed to solve forward and inverse problems involving PDEs. Rather than relying on large labeled datasets or traditional numerical solvers, PINNs incorporate physical constraints (such as PDE residuals and boundary conditions) directly into the loss function.

This project demonstrates:
- Solving nonlinear PDEs (e.g., Schrödinger, Allen-Cahn)
- Learning unknown parameters in PDEs (e.g., Navier-Stokes, KdV)
- Comparing continuous-time and discrete-time PINN formulations

---

## 🚀 Problems Addressed

### ✅ Continuous-Time PINNs
- **Nonlinear Schrödinger Equation**: Solved using a standard PINN with periodic boundary conditions and MSE-based loss.
- **Navier-Stokes Equation**: Identified unknown parameters and reconstructed the pressure field from sparse velocity data.

### ✅ Discrete-Time PINNs
- **Allen-Cahn Equation**: Solved using a Runge-Kutta-based architecture predicting the solution across large time steps.
- **KdV Equation**: Estimated unknown parameters by minimizing Runge-Kutta-based loss across time snapshots.

---

## 🗂️ File Structure

Implementing-PINNs-in-PyTorch/
├── schrodinger_pinn.py # PINN model for Schrödinger equation
├── allen_cahn_pinn.py # Runge-Kutta discrete-time model
├── navier_stokes_pinn.py # Inverse problem for Navier-Stokes
├── kdv_pinn.py # PINN parameter discovery for KdV
├── utils.py # Helper functions (sampling, plotting, etc.)
├── Project Report.pdf # Final project report (overview, results, references)
└── README.md # You are here


---

## 📊 Results Summary

| PDE | Method | Key Outcome |
|-----|--------|-------------|
| Schrödinger | Continuous PINN | Accurate solution with periodic boundary conditions |
| Allen-Cahn | Discrete-Time PINN | Final solution at \( t=0.9 \) accurately predicted from \( t=0.1 \) |
| Navier-Stokes | Inverse PINN | Parameters \( \lambda_1, \lambda_2 \) identified, pressure reconstructed |
| KdV | Parameter Discovery | Estimated parameters within 4% of ground truth |

---

## 🧪 Dependencies

Install dependencies:

pip install torch numpy matplotlib scipy

---

## 📚 References

- Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). _Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear PDEs._ Journal of Computational Physics, 378, 686–707.
- Psichogios, D. C., & Ungar, L. H. (1992); Lagaris, I. E., Likas, A., & Fotiadis, D. I. (1998, 2000); Karniadakis, G. E., et al. (2021)

See the [Project Report](./Project%20Report.pdf) for the complete bibliography.

---

## 📄 License

MIT License (see [`LICENSE`](./LICENSE)) file.

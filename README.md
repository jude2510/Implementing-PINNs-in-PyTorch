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

## 📚 References

- Raissi, M., Perdikaris, P., & Karniadakis, G. E. (2019). _Physics-informed neural networks: A deep learning framework for solving forward and inverse problems involving nonlinear PDEs._ Journal of Computational Physics, 378, 686–707.
- Psichogios, D. C., & Ungar, L. H. (1992); Lagaris, I. E., Likas, A., & Fotiadis, D. I. (1998, 2000); Karniadakis, G. E., et al. (2021)

See the [Project Report](./Project%20Report.pdf) for the complete bibliography.

---

## 📄 License

MIT License (see [`LICENSE`](./LICENSE)) file.

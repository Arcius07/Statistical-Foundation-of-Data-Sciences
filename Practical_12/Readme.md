# Metropolis Sampling Algorithm & Deterministic Modeling  
### Course Assignment – Python Implementation  
---

## 📌 Overview

This project contains the implementation of two core computational methods:

1. **Metropolis Algorithm (MCMC Sampling)**
2. **Deterministic Recursive Model**

Both programs are written in Python and executed in a single Colab/Jupyter notebook environment.  
The objective is to demonstrate the difference between *probabilistic sampling methods* and *deterministic iterative systems*.

---

## 🧠 Part A – Metropolis Sampling Algorithm

The Metropolis algorithm is a Markov Chain Monte Carlo (MCMC) method used to sample from complex probability distributions.  
In this implementation, the sampler targets the **standard normal distribution N(0,1)** using:

- Log-density formulation  
- Normal random-walk proposals  
- Burn-in phase  
- Thinning  
- Acceptance rate tracking  
- Statistical estimation from sampled values  

### 🔍 What the code computes

After generating the samples, the following statistics are calculated:

- **Acceptance Rate** → ratio of accepted proposals  
- **Sample Mean** → expected to be ~0  
- **Sample Variance** → expected to be ~1  
- **Deterministic estimate of E[X²]** → expected ≈ 1 for N(0,1)  

These results validate that the Metropolis sampler correctly approximates the standard normal distribution.

---

## ⚙️ Part B – Deterministic Model

This section implements a simple deterministic recurrence:


There is:
- No randomness  
- No probability  
- Fully predictable evolution  

This illustrates the contrast between stochastic and deterministic systems, showing how deterministic models always produce identical output for the same initial conditions.

---

## 🧪 Technologies Used

- **Language:** Python 3  
- **Libraries:** NumPy  
- **Environment:** Google Colab / Jupyter Notebook  

---

## ▶️ How to Run the Code

1. Open the `.ipynb` notebook (or Colab).  
2. Ensure NumPy is installed (`import numpy as np`).  
3. Run all cells top–bottom.  
4. Observe outputs for:
   - MCMC acceptance rate  
   - Estimated mean and variance  
   - Deterministic E[X²]  
   - Deterministic model sequence  

---

## 📊 Expected Output (Example)


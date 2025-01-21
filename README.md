# **Interference Prediction Using Gaussian Process Regression and Management Framework for Critical Services in Local 6G Networks**

Thank you for your interest in this repository! If you find the code or paper helpful, please consider citing our work:

### **Citation**
Shah, S. L., Mahmood, N. H., & Latva-aho, M. (2025). *Interference Prediction Using Gaussian Process Regression and Management Framework for Critical Services in Local 6G Networks*. In IEEE Wireless Communications and Networking Conference (WCNC), Mico Milano Congressi, Milan, Italy, March 24–27.


@inproceedings{shah2025interference,
  title={Interference Prediction Using Gaussian Process Regression and Management Framework for Critical Services in Local 6G Networks},
  author={Shah, Syed Luqman and Mahmood, Nurul Huda and Latva-aho, Matti},
  booktitle={IEEE Wireless Communications and Networking Conference (WCNC)},
  pages={},
  year={2025},
  organization={IEEE},
  address={Mico Milano Congressi, Milan, Italy},
  month={March},
  days={24--27}
}

---

### **Abstract**
Interference prediction and resource allocation are critical challenges in mission-critical applications where stringent latency and reliability constraints must be met. This paper proposes a novel Gaussian process regression (GPR)-based framework for predictive interference management and resource allocation in future 6G networks. Firstly, the received interference power is modeled as a Gaussian process, enabling both the prediction of future interference values and their corresponding estimation of uncertainty bounds. Differently from conventional machine learning methods that extract patterns from a given set of data without any prior belief, a Gaussian process assigns probability distributions to different functions that possibly represent the data set which can be further updates using Bayes' rule as more data points are observed. For instance, unlike deep neural networks, the GPR model requires only a few sample points to update its prior beliefs in real-time. Furthermore, we propose a proactive resource allocation scheme that dynamically adjusts resources according to predicted interference. The performance of the proposed approach is evaluated against two benchmarks prediction schemes, a moving average-based estimator and the ideal genie-aided estimator. The GPR-based method outperforms the moving average-based estimator and achieves near-optimal performance, closely matching the genie-aided benchmark.

---


## **Repository Overview**

This repository contains the simulation code and datasets for our paper. The repository is designed to support interference prediction and resource allocation for critical services in local 6G networks. Below is a breakdown of the provided files:

### **Files and Scripts**

1. **MATLAB Script: `Interference_signal.m`**
   - **Purpose**: Generates correlated interference signals. 
   - **Details**: 
     - Each sample value depends on the past `filterLength` values.
     - The correlation profile is defined by `filterCoefs` (e.g., uniform filter, Bessel function, Jakes model, etc.).
   - **Output**: 
     - If you cannot run this script, you can use the pre-generated dataset **`interference_200.csv`** included in this repository.

2. **MATLAB Script: `signal_only.m`**
   - **Purpose**: Simulates interference signals and creates a composite signal based on a specified Interference-to-Noise Ratio (INR).
   - **Details**: 
     - The generated signal is saved as a CSV file for further analysis.
   - **Output**: 
     - If you cannot run this script, you can use the pre-generated dataset **`signal_200.csv`** included in this repository.

3. **Python Notebook: `Interference-Prediction-Using-Gaussian-Process-Regression-for-Critical-Services-in-Local-6G-Networks.ipynb`**
   - **Purpose**: 
     - Implements **Gaussian Process Regression (GPR)** using the RBF kernel for interference prediction based on channel response data.
     - Dynamically allocates communication resources based on predicted and actual interference.
   - **Inputs**: 
     - `interference_200.csv` and `signal_200.csv` (generated by the MATLAB scripts).
   - **Outputs**:
     - **Performance Analysis Plots**: Achieved outage probability vs. target outage probability.
     - **Resource Usage Analysis Plots**: Resource usage vs. target outage probability.
     - Plots are saved as `.pdf` files for reference.

---

## **Steps to Use the Repository**

1. **MATLAB Simulations**
   - Run `Interference_signal.m` to generate the interference data or use the pre-generated file **`interference_200.csv`**.
   - Run `signal_only.m` to generate the signal data or use the pre-generated file **`signal_200.csv`**.

2. **Python Script**
   - Use the provided Jupyter Notebook to:
     - Perform GPR-based interference prediction.
     - Evaluate resource allocation efficiency.
     - Generate performance analysis plots.

3. **Outputs**
   - The Python notebook generates `.pdf` files with detailed analysis plots to evaluate performance and resource allocation strategies.

---

## **Contact Information**

If you need help reproducing the results or using this repository, feel free to reach out:

**Contact**: Syed Luqman Shah  
**Email**: sayedluqmans@gmail.com  

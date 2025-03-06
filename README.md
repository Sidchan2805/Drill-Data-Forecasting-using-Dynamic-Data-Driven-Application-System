📌 **Overview**

This project implements a Dynamic Data-Driven Application System (DDDAS) for real-time drill data forecasting. The methodology involves Higher-Order Singular Value Decomposition (HOSVD) for dimensionality reduction, Gaussian Process Regression (GPR) for modeling intermittent sensor data, and Reverse Order Particle Filtering (ROPF) to estimate values from incomplete real-time sensor data. Two versions of this implementation are provided, with slight variations in the noise levels and resampling techniques in the ROPF process. The surrogate model with gaussian process regression is trained on high fidelity simulation data. Then the Reverse order particle filter is used to generate better real-time estimates from incomplete sensor observations.

🚀 **Workflow**

1️⃣ Data Preprocessing:

Load and preprocess sensor data from CSV files.

Standardize features for consistency.

2️⃣ **Higher-Order Singular Value Decomposition (HOSVD):**

Transform the 3D spatio-temporal sensor data into a tensor representation.

Apply HOSVD to reduce dimensionality and extract meaningful features.

3️⃣ **Gaussian Process Regression (GPR):**

Train a Gaussian Process model to interpolate missing or intermittent sensor readings.

Perform regression across spatio-temporal domains.

4️⃣ **Reverse Order Particle Filtering (ROPF):**

Apply particle filtering to dynamically refine estimates with incoming real-time sensor data.

Two variations are implemented:

Version 1: Adjusts sensor noise level to 0.2.

Version 2: Implements systematic resampling for better state estimation.

🔧 Installation

Clone the repository and install dependencies:

git clone https://github.com/your-username/Drill-Data-Forecasting-DDDAS.git
cd Drill-Data-Forecasting-DDDAS
pip install -r requirements.txt

▶️ **Running the Project**

To run the entire pipeline:

python run_forecasting.py --input data/raw/sensor_readings.csv

Or open the Jupyter notebook:

jupyter notebook

📊 Results

Singular values from HOSVD for feature extraction.

Gaussian Process Regression plots comparing predicted vs. actual sensor values.

Reverse Order Particle Filtering output for real-time state estimation.

🔮 Future Improvements

Experiment with different kernel functions for Gaussian Process Regression.

Apply Bayesian Optimization for hyperparameter tuning.

Extend to deep learning-based spatio-temporal forecasting models.

📜 Citation

If you use this work, please consider citing it appropriately.

📌 Contributors

👤 Your Name📧 Email: sidchan2805@gmail.com🔗 GitHub: Sidchan2805


---
description: The smooth, sweet recipe we concoted.
icon: '3'
---

# Algorithms and Models used

The pipeline for analyzing PPG signals involves multiple stages, including feature extraction, model training, evaluation, and deployment, tailored for specific tasks such as estimating systolic blood pressure (SBP) and diastolic blood pressure (DBP). The process integrates advanced machine learning techniques and scalable deployment practices.

#### 1. Feature Extraction

Feature extraction focuses on deriving meaningful patterns from cleaned PPG signals. Time-domain features, such as mean, standard deviation, and pulse interval variability, capture statistical patterns in the signal. Frequency-domain features, extracted via techniques like Fast Fourier Transform (FFT), provide insights into the signal's spectral components, highlighting dominant frequencies linked to physiological conditions. Together, these features encapsulate the signal's temporal and spectral properties, forming the input for machine learning models.

#### 2. Model Training

For SBP prediction, a **NuSVR (Nu-Support Vector Regression)** model is employed. NuSVR is known for its robustness in handling complex, non-linear relationships, making it ideal for capturing the intricate dependencies between PPG features and blood pressure. For DBP prediction, **LGBMRegressor (Light Gradient Boosting Machine)** is utilized. LGBM is a gradient-boosting framework optimized for speed and efficiency, capable of handling large datasets while maintaining high accuracy. Both models are trained using datasets labeled with SBP and DBP measurements, with optimization focused on minimizing error metrics such as Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE). These metrics ensure the models achieve high precision and reliability.

#### 3. Evaluation and Deployment

Post-training, models are evaluated on test datasets to ensure generalizability. The selection of scalable models, such as NuSVR and LGBMRegressor, facilitates efficient deployment in real-world applications. These models are optimized for resource-constrained environments, ensuring real-time predictions in wearable devices. The pipeline’s scalability allows seamless integration into various platforms, advancing PPG-based health monitoring solutions.

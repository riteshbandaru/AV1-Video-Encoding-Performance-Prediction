# Machine Learning-Based Video Encoding Performance Prediction for AV1 Codec

A machine learning system that predicts CPU usage, encoding FPS, and RAM consumption for AV1 video encoding.

## Overview

This project uses machine learning to predict video encoding performance metrics based on encoding parameters and system specifications. The system achieved 93.68% accuracy for encoding FPS prediction and 94.76% accuracy for RAM usage prediction.

## Dataset

- **Training samples**: 10,615 encoding configurations
- **Test samples**: 2,648 independent test cases
- **Video resolutions**: 240p, 360p, 480p, 1080p
- **Encoder**: SVT-AV1 version 3.0.0

## Key Features

- Multi-output regression predicting 3 performance metrics
- 25 engineered features from raw encoding parameters
- Comparison of 5 machine learning algorithms (Random Forest, XGBoost, Gradient Boosting, Linear Regression, SVR)
- Feature importance analysis

## Results

| Target | Test R² Score | Performance |
|--------|---------------|-------------|
| Encoding FPS | 0.9368 | Excellent |
| RAM Usage | 0.9476 | Excellent |
| CPU Usage | -0.1518 | Poor* |

*CPU prediction failed due to single-core setup (98-99% usage consistently)

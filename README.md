# MoCap-anomaly-detection
## Overview
Welcome to the Motion Capture Anomaly Detection project! This project aims to detect anomalies in motion capture data using Variational Autoencoders (VAEs). By leveraging various VAE architectures, the project handles motion capture input data to achieve robust anomaly detection.

## Purpose
The goal is to develop an effective model for detecting anomalies in motion capture data, demonstrating the application of advanced deep learning techniques to real-world time-series data.

## Project Structure
### Data Used
Motion capture data sourced from publicly available datasets from Carnegie Mellon University. The data was post-processed and converted to .csv format. It was then separated into six smaller datasets: one for training and five others corresponding to different types of anomalies.

## Project Execution Schema

After preprocessing the motion capture data, different VAE architectures are trained to detect anomalies. Each architecture is evaluated based on its ability to detect anomalies, with non-walking data considered anomalous. Unlike point-wise anomaly detection, this project evaluates anomalies for entire recordings, requiring a robust solution capable of determining if the anomaly is severe enough to classify the whole file.

## VAE Architectures
### VAE (Variational Autoencoder)
![image](https://github.com/user-attachments/assets/da0bec57-e825-4288-944c-2a37eae497a1)

Purpose: The basic VAE is used for anomaly detection by learning the underlying data distribution. It captures the data's essential patterns and can identify deviations from these patterns.

Why it exists: VAEs provide a probabilistic approach to reconstructing input data, making them suitable for anomaly detection tasks.
### Conv-VAE (Convolutional VAE)
![image](https://github.com/user-attachments/assets/622dd860-451e-4244-893b-e12181a60a8c)

Purpose: Conv-VAEs are used for data with spatial structures, such as images or grid-based motion capture data.

Why it exists: By leveraging convolutional layers, Conv-VAEs can capture spatial hierarchies and local dependencies in the data, leading to better anomaly detection in structured data.
### FFT-VAE (Fast Fourier Transform VAE)
![image](https://github.com/user-attachments/assets/45b8394c-9c83-42f9-8e39-ae6f5b1886e6)

Purpose: FFT-VAEs apply Fourier Transform to the input data before feeding it into the VAE, capturing frequency domain information.

Why it exists: By transforming data into the frequency domain, FFT-VAEs can detect anomalies in periodic patterns and frequency components, which are often missed in the time domain.
### LSTM-VAE (Long Short-Term Memory VAE)
![image](https://github.com/user-attachments/assets/b4d4c9f2-12df-4bd6-a43a-8253d7f1cfac)

Purpose: LSTM-VAEs are designed for sequential data, such as time-series motion capture data, where temporal dependencies are critical.

Why it exists: LSTM layers within the VAE allow the model to understand and predict sequential patterns, making it ideal for time-series anomaly detection.


## Benefits of This Solution
- **Genrative approach**: In addition to being an effective anomaly detector, each trained network can generate human-like walking patterns.
- **Simpler Training Data Requirement**: By training only on normal walking patterns and still being able to detect anomalies, the solution simplifies data collection requirements.
- **System Tunability**: The output reconstruction error can be further thresholded by the user, enabling the algorithm to be more or less sensitive depending on user needs.
- **Full Recording Anomaly Detection**: Capable of detecting anomalies at certain points in time, the greatest achievement is determining if the entire recording should be considered anomalous.


## Possible Future Directions
- Implementing more advanced autoencoder-based networks.
- Auto-tuning the solution to increase usability for non-trained personnel.
- Training on other motion capture data to further refine performance.

## Contact
For inquiries, please contact krzy.miler@gmail.com.

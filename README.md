# outlier_detection
Outlier detection for research article titled "Synchronous Detection of Random and Event-based Anomalies in Environmental Time Series Data with Fourier Transformation and Deep Learning"


# Event-Driven Anomalies：
event-driven anomalies are defined by environmental policy regulations, resulting from significant and sustained changes in the monitored environment, such as natural disasters, abrupt weather changes, or pollution leakage. These anomalies are marked by periodic fluctuations over time, demonstrating continuity and predictability. Upon occurrence, the monitoring system is tasked with the comprehensive responsibility of prediction, reporting, response, and recording, termed event-driven monitoring data fluctuations (EDMDF) 
# Random Anomalies：
Stochastic anomalies are typically caused by random equipment malfunctions, human recording errors, or other random environmental factors. These anomalies often emerge suddenly and disappear just as quickly, characterized by their sheer randomness and discontinuity. The monitoring values for these anomalies do not align with the actual environmental conditions, clearly indicating erroneous recordings. These anomalies usually require deletion or smoothing during the recording and analysis phases, which are referred to as random anomalies (RA)


# Random Anomalies detector
## Data Smooth: Fourier Frequency Domain Filtration algorithm: 
Use 'RA_detector\preprocessing\Fourier_filter.py' to process individual variables, and then use 'RA_detector\preprocessing\assemble_filtered_data_by_fft_filter.py' to merge the processed individual variables into a DataFrame
## Data Smooth: SG Filter:
RA_detector\preprocessing\SG.py
## Data Smooth: SPAA:
RA_detector\preprocessing\SPAA.py
## Deep Learning
Construction of training and validation datasets (where the training set includes the test set used for testing during training):RA_detector\model\traindata_preparation.py  <br>
Model and its training: RA_detector\model\(GRU, LSTM, RNN, Seq2seq, TCN, Transformer).py
## RA Detector Framework
RA_detector\random_outlier.py

# Event-Driven Anomalies Detector
## The Data Prepare Before Feature Extraction
EDMDF_detector\feature_extract\base_dataset_create.py
## Feature Extraction: Frequency Domain Complex Feature Vectors:
EDMDF_detector\feature_extract\frequency_domain_complex_vector.py
## Feature Extraction: Fourier Coefficients:
EDMDF_detector\feature_extract\fourier_feature.py
## Feature Extraction: Statistics Feature
EDMDF_detector\feature_extract\stastic_feature.py
## Machine Learing
The data used for machine learning model training are derived from the feature extraction algorithm scripts in the EDMDF_detector\feature_extract folder. <br>
Model and its training: EDMDF_detector\model\(BPNN, CNN, GRU, lightbgm, LSTM, RF, SVM).py
## Event-Driven Anomalies Detector Framework
EDMDF_detector\event_outlier.py

# Total Framework
framework.py

# Sensitive Analysis
## Data Sample
Sobol sampling of the algorithm is required before performing sensitivity analysis <br>
Data sample script: sensitive_anal\data_sample.py
## Gaussian Process Regression Sensitivity Analysis: 
sensitive_anal\GPR.py
## Moment Independent Sensitivity Analysis:
sensitive_anal\MISA.py
## Sobol Total Effect Index:
sensitive_anal\sobol.py

# Contact us
## Address
Laboratory of Environmental Electrochemistry and Functional Materials (FunmatLab) ，School of Environmental Science and Engineering, Huazhong University of Science and Technology, 1037 Luoyu Road, Wuhan, Hubei Province, P.R. China 430074
## URL
http://funmat.ese.hust.edu.cn/

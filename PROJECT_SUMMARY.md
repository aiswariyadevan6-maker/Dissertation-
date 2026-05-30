# AI-Based Hybrid Network Intrusion Detection System
## Masters Project Summary

### Student Information
- Name: Aiswariya Akhil
- Student ID: E4318387
- Course: CIS4055 Computing Masters Project
- Supervisor: Nauman Issar

### Project Overview
This project implements a hybrid Network Intrusion Detection System (NIDS) combining:
- Random Forest (supervised learning) for known attack classification
- Autoencoder (unsupervised learning) for zero-day anomaly detection

### Key Results
| Metric | Random Forest | Hybrid Model |
|--------|--------------|--------------|
| Accuracy | 95.90% | 91.65% |
| Precision | 92.54% | 74.78% |
| Recall | 86.42% | 87.78% |
| F1-Score | 0.89 | 0.81 |
| False Positive Rate | 1.74% | 7.38% |
| False Negative Rate | 13.58% | 12.22% |

### How to Run
Activate environment: cd ~/Dissertation- && source venv/bin/activate
Train models: cd src/models && python train_simple.py
Evaluate: cd ../evaluation && python evaluation_simple.py

### Technologies Used
- Python 3.13
- Scikit-learn (Random Forest)
- TensorFlow/Keras (Autoencoder)
- Pandas, NumPy

### Conclusion
The hybrid model demonstrates improved recall for malicious traffic (87.78% vs 86.42%), showing that combining supervised and unsupervised learning enhances zero-day attack detection.

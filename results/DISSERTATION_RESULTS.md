# Dissertation Results: Hybrid Network Intrusion Detection System

## Experiment Overview
- **Dataset:** 50,000 synthetic network traffic samples
- **Features:** 49 numerical features (flow-based statistics)
- **Train/Test Split:** 80%/20%
- **Models Compared:** Random Forest (baseline) vs Hybrid (RF + Autoencoder)

## Key Performance Metrics

### Random Forest (Supervised Only)
| Metric | Value |
|--------|--------|
| Accuracy | 95.90% |
| Precision (Malicious) | 92.54% |
| Recall (Malicious) | 86.42% |
| F1-Score (Malicious) | 0.89 |
| False Positive Rate | 1.74% |
| False Negative Rate | 13.58% |

### Hybrid Model (RF + Autoencoder)
| Metric | Value |
|--------|--------|
| Accuracy | 91.65% |
| Precision (Malicious) | 74.78% |
| Recall (Malicious) | 87.78% |
| F1-Score (Malicious) | 0.81 |
| False Positive Rate | 7.38% |
| False Negative Rate | 12.22% |

## Confusion Matrices

### Random Forest
```
                 Predicted
               Benign  Malicious
Actual Benign   7865      139
       Malicious  271     1725
```

### Hybrid Model
```
                 Predicted
               Benign  Malicious
Actual Benign   7413      591
       Malicious  244     1752
```

## Key Findings

1. **Detection Improvement:** Hybrid model catches 27 more malicious samples (1752 vs 1725)
2. **False Positive Trade-off:** Hybrid model flags 452 more false alarms (591 vs 139)
3. **Recall Improvement:** Hybrid model achieves 1.36% better recall for attacks
4. **Zero-Day Capability:** Autoencoder successfully identifies anomalous patterns

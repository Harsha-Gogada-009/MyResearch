# MyResearch
# 🚗 Lane Change Prediction using Deep Learning  
*A Comprehensive Analysis with LSTMs, Transformers, Informer, and GNNs*  

## 📄 About the Paper  
This repository accompanies the research paper:  
**“From LSTMs to Transformers and GNNs: A Comprehensive Analysis on Lane Change Trajectory Forecasting”**  

The study presents a comparative and hybrid evaluation of deep learning architectures for **lane change prediction in autonomous vehicles**, focusing on:  
- **Recurrent Models**: GRU, Bi-LSTM, Attention-LSTM  
- **Attention-based Models**: Transformer, Informer  
- **Graph Neural Networks (GNNs)** for spatial interactions  
- **Hybrid Architectures**: Informer+LSTM, Informer+GNN, Transformer+GNN  

We benchmarked these models on the **NGSIM real-world trajectory dataset** and analyzed them under:  
- Clean vs noisy data  
- Rich vs minimal feature sets  
- Computational efficiency (GPU/CPU memory, training time)  

📌 **Novelty**: First-of-its-kind comparative study of hybrid Informer-based models with RNNs and GNNs for real-world lane-change forecasting.  

---

## 📊 Key Results  
| Model                  | Accuracy | Precision | Recall | F1 Score | Notes |
|------------------------|----------|-----------|--------|----------|-------|
| GRU                    | 66.7%    | 63.4%     | 63.5%  | 63.3%    | Baseline recurrent model |
| Bi-LSTM                | 78.5%    | 78.5%     | 77.6%  | 78.0%    | Captures bidirectional context |
| Attention-LSTM         | 89.4%    | 89.2%     | 88.9%  | 89.0%    | Attention improves robustness |
| Informer + Transformer | 98.0%    | 98.0%     | 97.9%  | 98.0%    | Strong long-sequence model |
| Informer + LSTM        | **98.5%** | 98.4%     | 98.5%  | **98.3%** | Best hybrid architecture |
| Informer + GNN         | 95.6%    | 95.7%     | 96.1%  | 95.1%    | Captures vehicle interactions |

---

## 🗂️ Dataset (https://github.com/Harsha-Gogada-009/NGSIM-Datasets)
We use the **NGSIM dataset**, which contains high-resolution vehicle trajectory data including:  
- Local/Global X, Y positions  
- Velocity, acceleration  
- Vehicle class, length, width  
- Lane ID  
- Preceding / Following vehicles  
- Space & Time Headway  

Labels:  
- `0` = Left Lane Change  
- `1` = Lane Keeping  
- `2` = Right Lane Change  

---

## ⚙️ Methodology  
### Preprocessing  
- Normalization via z-score standardization  
- Fixed-length sliding windows for temporal modeling  
- Lane change labels derived from Lane_ID shifts  

### Models Implemented  
- **GRU & Bi-LSTM**: Sequential baselines  
- **Attention-LSTM**: Selective focus on critical timesteps  
- **Transformer**: Self-attention for temporal dependencies  
- **Informer**: ProbSparse attention for long sequence forecasting  
- **Hybrid Models**: Informer+LSTM, Informer+GNN  

---
## ✨ Acknowledgements  

- Internship at **NIT Tiruchirappalli, Dept. of CSE**  
- Mentorship by **Dr. B. Nithya, Associate Professor**  
- Dataset: **NGSIM (Next Generation Simulation)**  

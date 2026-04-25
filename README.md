# Android-ransomware-detection
Tiểu luận An Toàn Thiết Bị Di Động
## Thông tin
- **Học phần:** An Toàn Thiết Bị Di Động
- **Bài báo gốc:** Android Ransomware Detection Using Supervised 
Machine Learning Techniques Based on Traffic Analysis
- **Tạp chí:** MDPI Sensors 2024
- **Link bài báo:** https://www.mdpi.com/1424-8220/24/1/189

## Dataset
- Nguồn: Kaggle
- Link: https://www.kaggle.com/datasets/subhajournal/android-ransomware-detection
- Số lượng: 392.034 bản ghi
- Số features: 86 cột
- Nhãn: Benign + 10 loại ransomware Android

## Các mô hình đã thực nghiệm
| Mô hình | Accuracy |
|---|---|
| Decision Tree | 74.38% |
| Ensemble | 74.21% |
| KNN | 64.92% |
| FNN | 58.93% |
| SVM | 54.71% |

## Kết quả
- Mô hình tốt nhất: **Decision Tree (74.38%)**
- Experiment 1: Toàn bộ 80 features
- Experiment 2: 19 features tốt nhất

## Cách chạy
1. Mở file `notebook.ipynb` trên Kaggle hoặc Google Colab
2. Gắn dataset từ Kaggle
3. Chạy từng cell theo thứ tự

## Môi trường
- Python 3.12
- scikit-learn
- TensorFlow/Keras
- pandas, numpy, matplotlib, seaborn

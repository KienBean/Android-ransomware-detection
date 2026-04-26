# Android Ransomware Detection

## Thông tin sinh viên
- **Họ tên:** Đỗ Trung Kiên
- **Lớp:** B9D54
- **SBD:** 11
- **Học phần:** An Toàn Thiết Bị Di Động

## Thông tin bài báo
- **Tên bài báo:** Android Ransomware Detection Using Supervised Machine Learning Techniques Based on Traffic Analysis
- **Tạp chí:** MDPI Sensors 2024
- **Link bài báo:** https://www.mdpi.com/1424-8220/24/1/189
- **DOI:** 10.3390/s24010189

## Dataset
- **Nguồn:** Kaggle
- **Link:** https://www.kaggle.com/datasets/subhajournal/android-ransomware-detection
- **Số lượng:** 392.034 bản ghi
- **Số features:** 86 cột
- **Nhãn:** Benign + 10 loại ransomware Android (SVpeng, PornDroid, Koler, RansomBO, Charger, Simplocker, WannaLocker, Jisut, Lockerpin, Pletor)

## Các mô hình thực nghiệm

### Experiment 1 — Toàn bộ features (80 features)
| Mô hình | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Decision Tree | 74.38% | 74.39% | 74.38% | 74.38% |
| Ensemble | 74.21% | 74.23% | 74.21% | 74.21% |
| KNN | 64.92% | 64.97% | 64.92% | 64.90% |
| FNN | 60.05% | 60.15% | 60.05% | 57.71% |
| SVM | 54.71% | 54.72% | 54.71% | 54.71% |

### Experiment 2 — 19 features tốt nhất
| Mô hình | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| Decision Tree | 68.59% | 68.59% | 68.59% | 68.58% |
| KNN | 67.38% | 67.43% | 67.38% | 67.37% |
| SVM | 52.00% | 52.00% | 52.00% | 51.90% |

### Mô hình cải tiến
| Mô hình | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| **Random Forest** | **76.83%** | - | - | - |
| XGBoost | 74.97% | - | - | - |

> **Random Forest đạt accuracy cao nhất 76.83%** — vượt trội so với tất cả mô hình gốc

## Kết quả biểu đồ
| Biểu đồ | Mô tả |
|---|---|
| phan_phoi_nhan.png | Phân phối các loại traffic trong dataset |
| feature_importance.png | Top 19 features quan trọng nhất (Decision Tree) |
| feature_importance_rf.png | Top 19 features quan trọng nhất (Random Forest) |
| bieu_do_loss_accuracy.png | Loss và Accuracy theo Epoch (FNN) |
| bang_ket_qua.png | Bảng so sánh kết quả các mô hình |
| confusion_matrix.png | Confusion Matrix - Decision Tree |
| confusion_matrix_all.png | Confusion Matrix tất cả mô hình gốc |
| confusion_matrix_cai_tien.png | Confusion Matrix mô hình cải tiến |
| so_sanh_experiment.png | So sánh Experiment 1 vs Experiment 2 |
| so_sanh_goc_vs_cai_tien.png | So sánh mô hình gốc vs mô hình cải tiến |

## Cách chạy
1. Vào **https://www.kaggle.com**
2. Tạo notebook mới
3. Gắn dataset: `android-ransomware-detection`
4. Copy code từ file `android-ransomware-detection.ipynb`
5. Nhấn **Run All**

## Môi trường
- Python 3.12
- scikit-learn
- XGBoost
- TensorFlow/Keras
- pandas, numpy, matplotlib, seaborn
- imbalanced-learn

## Kết luận
- Mô hình **Random Forest** (cải tiến) đạt kết quả tốt nhất với **76.83% accuracy**
- Experiment 1 (80 features) cho kết quả tốt hơn Experiment 2 (19 features)
- Phân tích Traffic mạng là phương pháp hiệu quả để phát hiện ransomware Android

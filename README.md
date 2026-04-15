# Project_QT
1. 🔍 Phân tích yêu cầu bài toán
Bài toán thực chất là gì?
Dự đoán giá hoặc xu hướng thị trường (stock/crypto)

Nhưng khác ML bình thường:
👉 Không chỉ dự đoán giá trị
👉 Mà còn dự đoán độ bất định (uncertainty)

Ý nghĩa:
Trong trading:

Dự đoán đúng nhưng không chắc chắn → không nên trade mạnh

Dự đoán + độ tin cậy cao → trade lớn hơn

👉 Đây là điểm ăn tiền của Bayesian Neural Network (BNN)

2. 🧠 Phương pháp giải quyết
2.1 Các hướng có thể dùng
(A) Neural Network thường
ANN / LSTM

❌ Không có uncertainty

(B) Monte Carlo Dropout
Approximate Bayesian

✔ Dễ implement

✔ Chạy nhanh

(C) Bayesian Neural Network (BNN) chuẩn
Dùng:

Variational Inference

Bayes by Backprop

✔ Có uncertainty thật sự

❌ Khó hơn

👉 Khuyến nghị:

Làm 2 model:

Baseline: LSTM hoặc ANN

Main: Bayesian NN hoặc MC Dropout

👉 Để phục vụ phần so sánh (requirement 4)

2.2 Tại sao chọn BNN?
Trading cần risk-aware decision

BNN cho:

Predictive mean (giá dự đoán)

Predictive variance (độ không chắc chắn)

👉 Giúp:

Position sizing

Risk management

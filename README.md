# Insurance Cost Prediction

## Tổng quan
Dự đoán phí bảo hiểm y tế (USD) dựa trên 5 đặc điểm nhân khẩu học và thói quen sinh hoạt: tuổi, giới tính, BMI, số con, tình trạng hút thuốc. Xử lý tập dữ liệu 1.338 bản ghi từ Kaggle.

## Công cụ & Quy trình
- **Công cụ:** Python (Pandas, Scikit-learn, Matplotlib, Seaborn).
- **Tiền xử lý:** Loại bỏ dữ liệu trùng lặp, mã hóa biến phân loại (Label Encoding cho `sex`, `smoker`). Kiểm tra giả định mô hình (tính độc lập, tuyến tính, không đa cộng tuyến).
- **Mô hình:** Hồi quy tuyến tính (Linear Regression).

## Kết quả
- **Hiệu năng:** R² = 0.8046, MAE = 4,198 USD, RMSE = 5,991 USD.
- **Insight:** Tình trạng hút thuốc (`smoker`) là yếu tố ảnh hưởng mạnh nhất (hệ số tương quan Pearson = 0.787). Người hút thuốc trả phí bảo hiểm cao hơn trung bình **23,051 USD** so với người không hút thuốc.

## Ý nghĩa thực tế
Với MAE ~4,200 USD (thấp hơn nhiều so với mức phí trung bình 13,200 USD), mô hình giúp:
- **Doanh nghiệp bảo hiểm:** Ước tính phí cơ bản và nhận diện nhóm khách hàng rủi ro cao.
- **Khách hàng:** Có cái nhìn tổng quan về mức tài chính cần chuẩn bị dựa trên hồ sơ sức khỏe.

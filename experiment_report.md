# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** AI20K-1234
**Name:** Nguyen Trong Tan
**Date:** 2026-6-10

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Agent: Based on my data, the best choice is Laptop at $1080.0. | 10 | Data is validated and correctly calculated. |
| Garbage Data (`garbage_data.csv`) | Agent Error: I'm choking on the data! (reduction operation 'argmax' not allowed for this dtype) | 1 | Mixing string ('ten dollars') with numbers broke the logic. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi sử dụng bộ dữ liệu rác (Garbage Data), Agent gặp nhiều vấn đề nghiêm trọng làm sai lệch hoặc gây lỗi hệ thống. Thứ nhất là lỗi kiểu dữ liệu (wrong data types) khi cột 'price' chứa chuỗi "ten dollars", khiến các hàm tính toán như `idxmax()` bị lỗi. Thứ hai, sự xuất hiện của các giá trị ngoại lai (outliers) như "Nuclear Reactor" với giá cực cao làm cho kết quả gợi ý không còn thực tế. Ngoài ra, việc thiếu kiểm soát các giá trị Null và Duplicate ID khiến Agent không thể truy xuất thông tin chính xác. Điều này minh chứng cho nguyên tắc "Garbage In, Garbage Out": AI dù thông minh đến đâu cũng sẽ đưa ra kết quả tồi nếu dữ liệu đầu vào không được làm sạch và kiểm soát chất lượng qua pipeline ETL.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

Đồng ý. Một Prompt tốt không thể cứu vãn được một hệ thống chạy trên nền dữ liệu sai lệch hoặc bị lỗi định dạng. Dữ liệu chất lượng là nền tảng cốt lõi để các mô hình AI/Agent hoạt động ổn định và chính xác.

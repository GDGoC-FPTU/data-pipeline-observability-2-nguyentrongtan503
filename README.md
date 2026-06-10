[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112958&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** tannt.ai20k@example.com
**Name:** Nguyen Trong Tan

---

## Mo ta

Trong bài Lab này, tôi đã xây dựng một hệ thống ETL tự động bằng Python và Pandas. Hệ thống thực hiện trích xuất dữ liệu từ JSON, kiểm tra tính hợp lệ (Validation), thực hiện biến đổi dữ liệu (Transformation) như tính giá giảm và chuẩn hóa tên danh mục, sau đó lưu kết quả ra CSV. Ngoài ra, tôi cũng thực hiện Stress Test để đánh giá ảnh hưởng của chất lượng dữ liệu đối với hiệu suất của AI Agent.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)

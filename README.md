[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112958&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** nguyentrongtan503@gmail.com
**Student ID:** AI20K-1234
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
python generate_garbage.py
python agent_simulation.py
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

Pipeline đã xử lý thành công 5 bản ghi từ `raw_data.json`. Kết quả thu được 3 bản ghi hợp lệ và 2 bản ghi bị loại bỏ (do giá âm hoặc thiếu category). Dữ liệu sau khi xử lý đã được chuẩn hóa, tính toán giá giảm và lưu trữ an toàn vào `processed_data.csv`.

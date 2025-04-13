# Detect-beans-seasons-1
Một mô hình sử dụng phiên bản YOLO vừa được ra mắt (YOLO v12m) đã được finetune trên các bộ datasets về hạt đậu (lấy link Google Drive về datasets ở phía dưới), nhằm tối đa hóa được số lượng chính xác nhất về số hạt đậu có trong hai ảnh đã được cho sẵn, mô hình này còn sử dụng thêm nhiều các phương pháp tiền xử lý ảnh nhằm làm tăng độ chính xác đến 97%.

## Giới thiệu
Số hạt đậu trong hai bức ảnh đã được đếm gần chính xác nhất bằng cách:
- **Sử dụng mô hình YOLO (v12m) đã được finetune trên 5 bộ datasets khác nhau về hạt đậu, 5 bộ dataset này được lấy trên roboflow.**
- **Sử dụng thêm nhiều phương pháp tiền xử lý hình ảnh để làm tăng thêm độ chính xác.**

## Yêu cầu
- **Python 3.7+**
- **Các thư viện Python:**
  - `opencv-python`
  - `ultralytics`
  - `mathplotplip`
  - `numpy`
  - `PIL`
  - `Path`
  - `shutil`
  - `yaml`

 ## Cài đặt
 
 1. **Clone repository:**

  ```bash
  git clone https://github.com/yourusername/your-project.git
  cd your-project
  ```

2. **Cài đặt các thư viện cần thiết:**
   
```bash
pip install opencv-python ultralytics mathplotplip numpy PIL-dotenv Path shutil yaml
```

3. **Chuẩn bị file mô hình YOLO:**

   Đảm bảo file mô hình (ví dụ `best.pt`) nằm trong thư mục dự án hoặc cập nhật đường dẫn chính xác trong code.

---

## Cấu trúc dự án

```
project
├── main.ipynb              # Code chính của dự án
├── best.pt                 # File mô hình YOLO đã fine-tuned (vì file best.pt khá nặng nên không thể upload lên github, file đã được đính kém trong link Google Drive datasets)
├── test.jpg                # Ảnh test dùng để đếm số hạt (ảnh test đã được crop lại so với ảnh gốc ban đầu để làm tăng độ chính xác của mô hình YOLO hơn)
└── README.md               # Tài liệu hướng dẫn dự án (README này)
```

---

## Train lại mô hình detection để đếm được chính xác số hạt
```
project
└──Train
    ├── datasets        # Dataset để train
    ├── datasets.ipynb  # Chạy file notebook để gộp 5 file datasets thành 1 file duy nhất    
    └── train.ipynb     # Chạy file notebook này để train lại mô hình
```
---

## Vui lòng truy cập link này để lấy datasets finetune cho mô hình YOLO v12m:
https://drive.google.com/drive/folders/18-1La3nzffX1qdyd23EIFcdIgW6kwnUt?usp=drive_link

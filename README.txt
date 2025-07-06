🔐 ĐỒ ÁN: AN TOÀN VÀ BẢO MẬT THÔNG TIN

Đây là đồ án mô phỏng việc gửi và nhận dữ liệu bảo mật giữa hai thực thể SENDER và RECEIVER,
sử dụng các kỹ thuật mã hóa và xác thực: RSA, SHA-256, zlib, và kiểm tra timestamp.

----------------------------------------
🚀 CHỨC NĂNG CHÍNH

- Sinh cặp khóa RSA cho Sender và Receiver.
- Mã hóa file văn bản (zlib), ký SHA-256, đóng gói gói tin có metadata và timestamp.
- Receiver kiểm tra integrity, timestamp chống replay attack.
- Giải nén, lưu file, phản hồi ACK/NACK cho Sender.

----------------------------------------
📁 CẤU TRÚC THƯ MỤC

Btl/
├── Generate_keys.py
├── Sender.py
├── Receiver.py
├── packet.json
├── Keys/
│   ├── Sender_pri.pem
│   ├── Sender_pub.pem
│   ├── Receiver_pri.pem
│   └── Receiver_pub.pem
├── Input/
│   └── finance.txt
├── Uploads/
│   └── received_finance.txt

----------------------------------------
🧪 HƯỚNG DẪN CHẠY

1. Cài thư viện:
    pip install pycryptodome

2. Chạy lần lượt:
    python Generate_keys.py
    python Sender.py
    python Receiver.py

----------------------------------------
👨‍🎓 THÔNG TIN SINH VIÊN

- Họ tên: Nguyễn Thế Vinh
- Lớp: Công nghệ thông tin – Đại học Đại Nam
- Đề tài: Bảo mật dữ liệu sử dụng RSA, SHA256, zlib và xác thực thời gian

----------------------------------------
🔒 KỸ THUẬT SỬ DỤNG

- RSA: Mã hóa công khai/riêng tư.
- SHA-256: Tạo mã băm xác thực.
- zlib: Nén và giải nén dữ liệu.
- timestamp: Chống replay attack.

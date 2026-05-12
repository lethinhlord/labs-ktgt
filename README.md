12 lab QIM/ST-QIM chạy tuần tự theo bước, có video MP4 mẫu, `guide.html` chuyên nghiệp, checkwork nhập mã sinh viên và tar riêng từng bài.

## Cách dùng nhanh

1. Tải file tar của bài cần thực hành trong thư mục `tars/`.
2. Import vào Labtainer:

```bash
imodule file:///duong/dan/01_qim_scalar.tar
```

3. Chạy lab theo đúng mã lab, ví dụ:

```bash
labtainer qim_scalar -r
```

4. Nếu cần mở thêm cửa sổ terminal của container:

```bash
moreterm.py qim_scalar qimlab
```

5. Khi lab mở, xem `guide.html` để làm tuần tự trong terminal `qimlab`:

```bash
python3 run_lab.py --step 1
python3 run_lab.py --step 2
python3 run_lab.py --step 3
python3 run_lab.py --step 4
python3 run_lab.py --step 5
checkwork
```

6. Dừng lab sau khi hoàn thành:

```bash
stoplab
```

Mỗi lab có `guide.html`, mô hình Labtainer trực quan, bảng câu lệnh chuẩn, `docs/<lab>.html`, `NOTE.txt`, video `media/sample_video.mp4`, `run_lab.py`, cấu hình Labtainer và checkwork riêng.

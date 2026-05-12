12 lab QIM/ST-QIM chạy tuần tự theo bước, có video MP4 mẫu, `guide.html` chuyên nghiệp, checkwork nhập mã sinh viên và tar riêng từng bài.

## Cách dùng nhanh

1. Tải file tar của bài cần thực hành trong thư mục `tars/`.
2. Import vào Labtainer:

```bash
imodule file:///duong/dan/01_qim_scalar.tar
```

3. Chạy lab theo đúng mã lab, ví dụ:

```bash
labtainer -r qim_scalar
```

4. Khi Labtainer khởi tạo thành công và hỏi thông tin chấm bài, nhập mã sinh viên rồi ấn Enter để vào lab. Các cửa sổ/terminal cần thiết sẽ mở ra.

5. Labtainer tự mở terminal `qimlab` theo cấu hình `TERMINALS 1`; người học không cần tự mở thêm cửa sổ.

6. Khi lab mở, xem `guide.html` để làm tuần tự trong terminal `qimlab` bằng lệnh Linux chuẩn:

```bash
mkdir -p work
pwd
ls -lh
ls -lh media/sample_video.mp4
sha256sum media/sample_video.mp4 | tee work/video_sha256.txt
python3 run_lab.py theory | tee work/theory.log
python3 run_lab.py prepare | tee work/prepare.log
python3 -m json.tool work/step2_chuan_bi_tham_so_va_du_lieu_nhi_phan.json | tee work/step2_view.txt
python3 run_lab.py embed | tee work/embed.log
python3 -m json.tool work/step3_thuc_hien_nhung_qim_stqim.json | tee work/step3_view.txt
python3 run_lab.py extract | tee work/extract.log
python3 -m json.tool work/step4_tach_tin_va_do_chat_luong.json | tee work/step4_view.txt
python3 run_lab.py report | tee work/report.log
cat work/summary.txt
python3 -m json.tool work/result.json | tee work/result_view.txt
checkwork
```

7. Dừng lab sau khi hoàn thành:

```bash
stoplab
```

Mỗi lab có `guide.html` được chuẩn hóa theo mẫu, mô hình Labtainer trực quan, phần lý thuyết QIM/ST-QIM chi tiết, quy trình nhập mã sinh viên trước khi vào lab, bảng câu lệnh Linux chuẩn, `docs/<lab>.html`, `NOTE.txt`, video `media/sample_video.mp4`, `run_lab.py`, cấu hình Labtainer và checkwork riêng.

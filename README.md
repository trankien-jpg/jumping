# Jumpscare Web Prank 👻

Trang web trò đùa vui (jumpscare) thuần HTML, CSS, JavaScript được tối ưu cho cả máy tính và điện thoại di động (iOS Safari, Android Chrome).

## 📁 Cấu trúc thư mục

```text
jumpscare/
  ├── index.html          # Mã nguồn chính (HTML/CSS/JS thuần, không thư viện ngoài)
  ├── assets/
  │   ├── scare.jpg       # Ảnh hù dọa
  │   └── scare.mp3       # Âm thanh hét kinh dị
  └── README.md           # Hướng dẫn chi tiết
```

## ⚙️ Tùy chỉnh (CONFIG)

Mở file `index.html`, bạn sẽ thấy đối tượng `CONFIG` ngay đầu thẻ `<script>`:

```javascript
const CONFIG = {
  delayMinMs: 2000,           // Thời gian chờ tối thiểu (2 giây)
  delayMaxMs: 5000,           // Thời gian chờ tối đa (5 giây)
  imageDurationMs: 3000,      // Thời gian hiện jumpscare (3 giây)
  volume: 1.0,                // Âm lượng (0.0 đến 1.0)
  imageSrc: './assets/scare.jpg',
  soundSrc: './assets/scare.mp3',
  lureText: 'Có một video dành cho bạn',
  buttonText: 'Bấm để xem',
  endText: 'Đùa thôi! 👻',
  replayButtonText: 'Xem lại'
};
```

## 🔄 Cách thay thế ảnh và âm thanh

- Đặt file ảnh mới vào thư mục `assets/` và đặt tên là `scare.jpg` (hoặc đổi đường dẫn trong `imageSrc`).
- Đặt file âm thanh mới vào thư mục `assets/` và đặt tên là `scare.mp3` (hoặc đổi đường dẫn trong `soundSrc`).
- Nếu chưa có file hoặc file bị lỗi tải, trang sẽ tự động kích hoạt chế độ **dự phòng (fallback)**: mặt quỷ vẽ bằng vector SVG và âm thanh tần số cao ghê rợn bằng Web Audio API.

## 🚀 Đẩy bản cập nhật lên GitHub Pages

Mỗi khi chỉnh sửa xong code hoặc thay ảnh/âm thanh, chạy các lệnh git sau trong thư mục `jumpscare/`:

```bash
git add .
git commit -m "Cập nhật tài nguyên và cấu hình"
git push origin main
```

# Smart Redirect Landing Page

Dự án này là một trang web tĩnh (Static Web) sử dụng HTML, CSS (Tailwind qua CDN) và JavaScript thuần.

## Cấu trúc thư mục
- `index.html`: Trang Landing Page chính với chủ đề Review Sức khỏe/Bài tập.
- `plugin.html`: Trang mô phỏng hệ thống Captcha Cloudflare.

## Các tính năng chính
- **Giao diện hiện đại**: Responsive 100%, tích hợp hiệu ứng scroll reveal và Google Maps.
- **Smart Redirect (Chặn gclid)**: Bất cứ khi nào URL có chứa chuỗi tham số `gclid=`, trình duyệt sẽ bị chặn render bằng JavaScript và lập tức chuyển qua `https://mamakana.com/?ref=qihttegh`. Logic này được đặt ở ngay dòng đầu tiên của thẻ `<head>`.
- **Captcha giả lập**: Nút "Verify you are human" ở `plugin.html` cũng sẽ trỏ thẳng tới Target Link khi được click.

## Hướng dẫn chạy ở Local
Vì là trang web tĩnh hoàn toàn (không cần NodeJS hay server Java):
1. Bạn chỉ cần click đúp vào file `index.html` hoặc `plugin.html` để mở bằng trình duyệt (Chrome/Edge/Safari).
2. Khi mở file, đuôi URL trên trình duyệt ví dụ: `file:///.../index.html`. Hãy thử thêm `?gclid=123` vào cuối (thành `file:///.../index.html?gclid=123`) và ấn Enter để xem khả năng chuyển hướng tức thì.

## Hướng dẫn Deploy lên Host (Miễn phí 100%)

### 1. Dùng Vercel hoặc Netlify
- Đăng nhập vào [Vercel](https://vercel.com) hoặc [Netlify](https://netlify.com).
- Kéo thả thư mục chứa `index.html` và `plugin.html` vào giao diện deploy của họ (hoặc push thư mục này lên GitHub và liên kết repository).
- Hệ thống sẽ tự cấp cho bạn 1 đường link trang web public có hỗ trợ sẵn HTTPS cực kì nhanh nhẹn.

### 2. Dùng GitHub Pages
- Tạo 1 repository trên GitHub (VD: `my-landing-page`).
- Upload 2 file HTML lên.
- Vào phần **Settings** của repo -> **Pages** -> Chọn nhánh deploy là `main` (hoặc `master`).
- GitHub sẽ cung cấp link dạng `https://[username].github.io/my-landing-page/`.

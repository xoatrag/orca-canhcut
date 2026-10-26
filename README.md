# Orca × Canhcut: Vũ trụ nhỏ của chúng mình
Kho lưu trữ cá nhân chạy hoàn toàn trên trình duyệt, viết bằng HTML/CSS/JS thuần. Không máy chủ, không gọi dịch vụ bên ngoài, không thư viện phụ thuộc.

## Chạy thử trên Windows
1. Giải nén thư mục `orca-canhcut`.
2. Cách đơn giản: nhấp đúp `index.html`. Cách ổn định hơn: mở PowerShell trong thư mục, chạy `python -m http.server`, rồi mở http://localhost:8000.
3. Thêm một kỷ niệm, tải lại trang (F5) và kiểm tra dữ liệu vẫn còn.
4. Thêm một ảnh (mục Album ảnh), rồi vào "Sao lưu và cài đặt" để tải bản sao lưu.

## Đưa lên GitHub Pages
1. Tạo tài khoản GitHub miễn phí, chọn New repository (đặt Public, vì gói miễn phí cần repo công khai).
2. Chỉ tải lên: `index.html`, `styles.css`, `app.js`, `README.md` và thư mục `assets`. TUYỆT ĐỐI không tải file sao lưu .json hay ảnh cá nhân.
3. Vào Settings > Pages > Source: "Deploy from a branch", nhánh `main`, thư mục `/ (root)` > Save.
4. Chờ khoảng một phút, mở đường dẫn GitHub hiển thị. Mọi đường dẫn trong mã đều là tương đối nên chạy được dưới dạng USERNAME.github.io/REPOSITORY/.
5. Mở trên điện thoại. Lần đầu dữ liệu sẽ TRỐNG: dữ liệu gắn với từng trình duyệt và từng thiết bị. Muốn chuyển dữ liệu, dùng Sao lưu rồi Khôi phục.

Gỡ lỗi: trang trắng thì kiểm tra tên file viết thường và nằm ở thư mục gốc; mất hình mascot thì thiếu thư mục `assets`; không lưu được thì có thể đang dùng chế độ riêng tư hoặc đã tắt lưu trữ.

## Quyền riêng tư
Trang công khai chỉ chứa mã nguồn. Nhật ký của bạn nằm trong IndexedDB của trình duyệt. Ứng dụng không có mật khẩu: ai dùng được hồ sơ trình duyệt này đều đọc được. Xóa dữ liệu trang web sẽ mất hết, vì vậy hãy xuất sao lưu thường xuyên, cất bản sao ở nơi khác và thử khôi phục.

## Danh sách kiểm tra thủ công
- [ ] Thêm, sửa, xóa mỗi loại: kỷ niệm, về chúng mình, ảnh, album
- [ ] Thêm 2 ảnh, mở xem phóng to, liên kết một ảnh với kỷ niệm, xóa một ảnh
- [ ] Tải lại trang: dữ liệu vẫn còn
- [ ] Lọc theo danh mục, người, thẻ; tìm kiếm có chọn khoảng ngày
- [ ] Tải sao lưu, xóa toàn bộ dữ liệu, nhập lại (chế độ Gộp), kiểm tra liên kết và ảnh còn nguyên
- [ ] Thử nhập một file .json bất kỳ: ứng dụng phải từ chối
- [ ] Thử ở cửa sổ hẹp như điện thoại và chỉ dùng phím Tab

## Chưa kiểm thử và hạn chế
Mã chưa được chạy thử trong trình duyệt thật, hãy làm theo danh sách trên trước khi dùng. Chưa có: trang hồ sơ riêng có ảnh đại diện (mục "Về chúng mình" lọc theo người), sao lưu ZIP (chỉ JSON), đính kèm file trong Tử vi (hãy dùng Ảnh), sắp xếp giai đoạn (giai đoạn là nhãn tự gõ), cảnh báo chưa lưu khi bấm liên kết trong ứng dụng (chỉ khi đóng tab). Thư viện ảnh rất lớn sẽ làm file JSON nặng. Hình Orca và chim cánh cụt còn đơn giản, có thể tinh chỉnh thêm.

Tôi xem qua index.html và ket-qua.html, và có 1 lỗi lớn nhất + một vài điểm cần chỉnh.

1) Lỗi lớn: đường dẫn CSS sai
Ở cả hai file đều có dòng như này:

index.html
ket-qua.html

Đây là đường dẫn tuyệt đối theo máy Windows, không hợp lệ khi website chạy trên máy khác hoặc trên server. Với HTML, nên dùng đường dẫn tương đối:


Tương tự cho cả trang kết quả.

Nếu bạn mở file trên máy khác, CSS sẽ không load được, giao diện sẽ trông rời rạc hoặc mất style.

2) Cùng một tệp nhưng tên khác nhau
Trong header bạn viết:


Nhưng ở phần giới thiệu lại là:


Điều này không làm hỏng chức năng, nhưng nhìn không nhất quán về brand/name.

3) Form GET sẽ hiện dữ liệu lên URL
Trong index.html:


Với method="get", dữ liệu người dùng sẽ hiển thị trên thanh địa chỉ. Đây không phải lỗi, chỉ là cách hoạt động của GET. Nếu muốn “ẩn” dữ liệu, nên dùng method="post".

4) Trang kết quả chưa có style riêng
Trong ket-qua.html, bạn dùng class .result-main và .result-panel, nhưng trong style.css tôi không thấy định nghĩa các class này. Không phải lỗi runtime, nhưng trang sẽ không có layout đẹp như mong muốn.

Nên sửa ngay
Mình khuyên sửa trước tiên là 2 chỗ này:

index.html: đổi href="D:\CNTT20-04\portfolio\css\style.css" thành href="css/style.css"
ket-qua.html: đổi tương tự
Nếu bạn muốn, tôi có thể sửa luôn cho bạn và làm lại cho đúng toàn bộ project.
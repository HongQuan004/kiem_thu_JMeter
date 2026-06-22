# Báo cáo Thực hành Kiểm thử API với Apache JMeter
# Họ và tên: Nguyễn Hồng Quân 
# Mã sinh viên: 22010123

1. Thông tin chung <br>
Công cụ kiểm thử: Apache JMeter (Phiên bản 5.6.3) <br>
Mục tiêu: Thực hành gửi HTTP Request và tự động kiểm tra kết quả trả về (Assertion). <br>
API sử dụng: https://jsonplaceholder.typicode.com/users <br>

Phương thức: GET <br>
2. Kịch bản kiểm thử (Test Cases) <br>
2.1. Cấu hình HTTP Request cơ bản <br>
Thiết lập kịch bản gửi một GET request tới server để lấy danh sách người dùng. <br>

Protocol: https <br>
Server Name: jsonplaceholder.typicode.com <br>
Path: users <br>
Hình ảnh cấu hình HTTP Request: Cấu hình HTTP Request <br>
<img width="1527" height="865" alt="image" src="https://github.com/user-attachments/assets/4732bf4b-c9b4-4caf-8e7e-25b7df47b435" />

2.2. Kiểm thử tự động (Pass Case - Kỳ vọng 200 OK) <br>
Mục tiêu: Đảm bảo API hoạt động bình thường và trả về mã trạng thái 200. <br>
Sử dụng Response Assertion để kiểm tra Response Code với giá trị 200. <br>
Kết quả: Kịch bản chạy thành công (hiển thị màu xanh trong View Results Tree). <br>
Hình ảnh cấu hình Assertion (200): Cấu hình Assertion 200 <br>
<img width="1512" height="848" alt="image" src="https://github.com/user-attachments/assets/3df9a8d3-45f2-432d-a51a-26c30204afc7" />

Hình ảnh kết quả chạy thành công: Kết quả Pass
<img width="1514" height="862" alt="image" src="https://github.com/user-attachments/assets/90f9273c-4414-4549-a294-f8d6f62a191e" />

2.3. Kiểm thử tự động (Fail Case - Cố tình tạo lỗi) <br>
Mục tiêu: Thay đổi điều kiện kiểm tra để đảm bảo công cụ bắt được lỗi khi kết quả không đúng kỳ vọng. <br>
Đổi Response Assertion sang kỳ vọng mã 900. <br>
Kết quả: Kịch bản báo lỗi (hiển thị màu đỏ) do mã thực tế trả về là 200 chứ không phải 900 như kịch bản yêu cầu.<br>
Hình ảnh cấu hình Assertion (900): Cấu hình Assertion 900
<img width="1507" height="864" alt="image" src="https://github.com/user-attachments/assets/b1719e69-15a2-438f-b717-fa8f6ebe9ff8" />


Hình ảnh kết quả báo lỗi: Kết quả Fail

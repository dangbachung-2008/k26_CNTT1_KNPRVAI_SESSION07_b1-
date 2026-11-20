# [Bài thực hành 6] Xây dựng báo cáo phân tích kết quả học tập từ nhiều tài liệu
 **Các Prompt dùng để đọc và xử lý 4 file.**
- **1. Prompt đọc File 1 – Danh sách sinh viên** 
Bạn là trợ lý xử lý dữ liệu đào tạo.
Hãy đọc File 1 chứa danh sách 30 sinh viên và trích xuất thông tin thành bảng có cấu trúc.
Yêu cầu đầu ra:
STT
Mã sinh viên
Họ và tên
Quy định:
-   Giữ nguyên chính xác mã sinh viên và họ tên trong file.
-   Sử dụng mã sinh viên làm khóa định danh chính.
-   Phát hiện các mã sinh viên bị trùng.
-   Phát hiện sinh viên trùng họ tên nhưng khác mã sinh viên. 
-   Đánh dấu thông tin bị thiếu.
-   Không tự ý sửa đổi hoặc suy đoán dữ liệu.  
Cuối cùng, thống kê tổng số sinh viên và danh sách các trường hợp bất thường.
- **2. Prompt đọc File 2 – Điểm chuyên cần và bài tập**
Bạn là chuyên gia xử lý dữ liệu điểm số.
Hãy đọc File 2 chứa kết quả điểm chuyên cần và điểm bài tập của sinh viên.
Trích xuất dữ liệu thành bảng:
Mã sinh viên
Điểm chuyên cần
Điểm bài tập
Yêu cầu:
-   Giữ nguyên mã sinh viên.
-   Điểm chuyên cần và điểm bài tập phải nằm trong khoảng 0–10.   
-   Kiểm tra các bản ghi bị trùng mã sinh viên.
-   Phát hiện sinh viên bị thiếu điểm chuyên cần hoặc điểm bài tập.
-   Đánh dấu "Thiếu dữ liệu" đối với điểm không có trong file.  
-   Không tự điền hoặc suy đoán điểm.
-   Không ghép dữ liệu dựa trên họ tên.
Cuối cùng, thống kê số lượng bản ghi hợp lệ, bản ghi trùng và bản ghi thiếu dữ liệu.
**3. Prompt đọc File 3 – Điểm kiểm tra giữa kỳ**

Bạn là trợ lý phân tích dữ liệu giáo dục.
Hãy đọc File 3 chứa kết quả kiểm tra giữa kỳ của 30 sinh viên.
Trích xuất dữ liệu thành bảng:
Mã sinh viên
Điểm giữa kỳ
Yêu cầu:
-   Giữ nguyên mã sinh viên và điểm số.
-   Điểm phải nằm trong khoảng 0–10.
-   Phát hiện mã sinh viên bị trùng.
-   Phát hiện sinh viên chưa có điểm giữa kỳ.
-   Đánh dấu "Thiếu dữ liệu" nếu không có điểm.
-   Không tự tạo hoặc bổ sung điểm.
-   Không ghép dữ liệu chỉ dựa trên họ tên.
Cuối cùng, thống kê số sinh viên có điểm, số sinh viên thiếu điểm và các trường hợp dữ liệu bất thường.

 **4. Prompt đọc File 4 – Điểm cuối kỳ và nhận xét giảng viên**

Bạn là chuyên gia xử lý dữ liệu đào tạo.
Hãy đọc File 4 chứa điểm thi cuối kỳ và nhận xét của giảng viên.
Trích xuất dữ liệu thành bảng:
Mã sinh viên
Điểm cuối kỳ
Nhận xét giảng viên
Yêu cầu: 
-   Giữ nguyên chính xác mã sinh viên.
-   Giữ nguyên điểm cuối kỳ và nội dung nhận xét.
-   Điểm phải nằm trong khoảng 0–10.
-   Phát hiện dữ liệu trùng lặp.
-   Phát hiện sinh viên thiếu điểm cuối kỳ.
-   Đánh dấu "Thiếu dữ liệu" nếu không có điểm.
-   Không tự ý sửa nhận xét hoặc suy đoán nguyên nhân điểm thấp.
-   Không ghép dữ liệu chỉ dựa trên họ tên.
Cuối cùng, thống kê số sinh viên có điểm cuối kỳ, số sinh viên thiếu điểm và các trường hợp bất thường.

 **2. Prompt đối chiếu dữ liệu**
 Bạn là chuyên gia phân tích dữ liệu giáo dục.
Hãy đối chiếu dữ liệu từ 4 file đã trích xuất.
Yêu cầu:
1.  Sử dụng mã sinh viên làm khóa chính.
2.  Không ghép dữ liệu bằng họ tên.
3.  Tổng hợp đủ 30 sinh viên. 
4.  Phát hiện sinh viên thiếu điểm ở từng đầu điểm.
5.  Phát hiện mã sinh viên bị trùng.
6.  Phát hiện thông tin họ tên không thống nhất.
7.  Không tự tạo hoặc điền dữ liệu còn thiếu
Công thức tính điểm:
Tổng kết = Chuyên cần × 10% + Bài tập × 20% + Giữa kỳ × 30% + Cuối kỳ × 40%.
Phân loại:
-   Tổng kết từ 5,0 trở lên: Đạt.
-   Tổng kết dưới 5,0: Chưa đạt.
-   Thiếu bất kỳ đầu điểm nào: Thiếu dữ liệu, chưa phân loại đạt/chưa đạt.
Làm tròn điểm tổng kết đến 2 chữ số thập phân.
Xuất bảng gồm:  
Mã SV, Họ tên, Chuyên cần, Bài tập, Giữa kỳ, Cuối kỳ, Tổng kết, Kết quả.
Sau đó lập danh sách bất thường và thống kê kết quả toàn lớp.

**Bảng kết quả tổng hợp 30 sinh viên gồm: Mã SV, Họ tên, Chuyên cần, Bài tập, Giữa kỳ, Cuối kỳ, Tổng kết, Kết quả.**

| STT | Mã SV | Họ tên | Chuyên cần | Bài tập | Giữa kỳ | Cuối kì |  Tổng  | kết quả | 
| :----: | :----: | :----: | :----: | :----: | :----: | :----: | :----:|  :----: | 
| 1 | SV001 | Nuyễn Văn An | 9 | 8 | 8 | 8 |  8,20 | đạt | 
| 2 | SV002 | Trần Thị Bình | 8 | 7 | 7 | 6 | 6,70 | đạt |
| 3 | SV003 | Lê Văn Cường | 7 | 8 | 6 | 7 | 6,90 | đạt | 
| 4 | SV004| Phạm Thị Dung | 10 | 9 | 9 | 9 | 9,20 | đạt |
| 5 | SV005 | Hoàng Văn Đức | 6 | 6 | 5 | 5 | 5,20 | đạt | 
| 6 | SV006 | Đỗ Thị Hà | 9 | 8 | 7 | 8 | 7,90 | đạt | 
| 7 | SV007 | Bùi Văn Hùng | 5 | 6 | 4 |4 | 4,59 | chưa đạt | 
| 8 | SV008 | Nguyễn Thị Lan | 8 | 9 | 8 | 9 | 8,60 | đạt | 
| 9 | SV009 | Trần Văn Minh | 7 | 7 | 7 | 7 | 7,00 | đạt |
| 10| SV010 | Lê Thị Ngọc | 9 | 8 | 9 | 8 | 8,50 | đạt |
| 11 | SV011 | Phạm Văn Nam | 6 | 5 | 5 | 4 | 4,50 | chưa đạt | 
|12 | Sv012 | Hoàng Thị Oanh | 8 | 8 | 7 | 7 | 7,40 | đạt | 
| 13 | SV013 | Đỗ Văn phúc | 7 | 6 | 6 | 6 | 6,10 | đạt | 
| 14 | SV014 | Bùi thị Quỳnh | 10 | 9 | 8 | 9 | 8,90 | đạt | 
| 15 | SV015 | Nguyễn Văn Sơn | 5 | 5 | 6 | 5 |5,20 | đạt |
| 16 | SV016 | Trần Thị Thảo | 9 | 9 | 9 | 10 | 9,40  | đạt | 
| 17 | Sv017 | Lê Văn Tuấn | 7 | 5 | 5 | 4 | 4,60 | chưa  đạt | 
| 18 | SV018 | Phạm Thị Uyên | 8 | 7 | 8 | 7 | 7,40 | đạt | 
| 19 | SV019 | Hoàng Văn Việt | 6 | 7 | 6 | 6 | 6,20 | đạt | 
| 20 | SV020 | Đỗ Thị Xuân | 9 | 8 | 8 | 9 | 8,60 | đạt | 
| 21 | SV021 | Bùi Văn Long | 7 | 7 | 5 | 5 |5,60 | đạt |
| 22 | SV022 | Nuyễn Thị Mai | 8 | 9 | 9 | 8 | 8,50 | đạt | 
| 23 | SV023 | Trần Văn Bình | 6 | 6 | 4 | 5 | 4,90 | chưa đạt |
| 24 | SV024 | Lê Thị Hương | 10 |  8 | 9 | 9 | 9,00 | đạt | 
| 25 | SV025 | Phạm Văn Khánh | 7 | 8 | 7 | 6 | 6,80 | đạt | 
| 26 | SV026 | Hoàng Thị Linh | 8 | 8 | 8 | 8 | 8,00 | đạt | 
| 27 | SV027 | Dỗ Văn Thành | 5 | 6 | 5 | 4 | 4,50 | chưa đạt | 
| 28 | SV028 | Bùi Thị Trang | 9 | 9 | 8 | 9 | 8,80 | đạt | 
| 29 | SV029 | Nguyễn Văn Phong | 7 | 7 | 8 | 7 | 7,30 | đạt | 
| 30 | SV030 | Trần Thị Yến | 8 | 7 | 6 | 7 | 6,90 | đạt | 
 **4 BÁO CÁO THỐNG KÊ TỶ LỆ ĐẠT VÀ CHƯA ĐẠT**
Tổng số sinh viên: 30 sinh viên.

 **1. Bảng thống kê kết quả**
 | STT |  Kết Quả | Số sinh viên | tỉ lệ | 
 | :----: | :----: | :----: | :----: | 
 | 1 | đạt | 25 | 83,33% |
 | 2 | chưa đạt | 5 | 16,67% | 

**5 . DANH SÁCH CÁC TRƯỜNG HỢP BẤT THƯỜNG**

| STT |  Mã sinh viên | loại bất thường  | thông tin chi tiết | 
| :----: | :----: | :----: | :----: | 
| 1 | SV007  | Điểm thấp |  Tổng kết 4,50 – Chưa đạt | 
| 2 | SV011 | Điểm thấp | Tổng kết 4,50 – Chưa đạt | 
| 3 | SV017 | Điểm thấp | Tổng kết 4,60 – Chưa đạt | 
| 4 | SV023 |  Điểm thấp | Tổng kết 4,90 – Chưa đạt | 
| 5 | SV027 | Điểm thấp  | Tổng kết 4,50 – Chưa đạt | 

**5 BÁO CÁO NHẬN XÉT TÌNH HÌNH HỌC TẬP CỦA LỚP**

 **1. Tổng quan kết quả học tập**
Qua quá trình tổng hợp và tính điểm của 30 sinh viên môn Nhập môn Java, kết quả cho thấy tình hình học tập của lớp nhìn chung khá tốt. Điểm tổng kết được tính theo công thức: điểm chuyên cần chiếm 10%, điểm bài tập chiếm 20%, điểm giữa kỳ chiếm 30% và điểm cuối kỳ chiếm 40%. Sinh viên đạt từ 5,0 điểm trở lên được xếp loại Đạt; dưới 5,0 điểm được xếp loại Chưa đạt.
Kết quả thống kê cho thấy có 25/30 sinh viên đạt yêu cầu, chiếm 83,33%. Có 5/30 sinh viên chưa đạt, chiếm 16,67%. Như vậy, phần lớn sinh viên đã đáp ứng được yêu cầu của học phần. Đây là kết quả tương đối tích cực, tuy nhiên vẫn còn một số sinh viên cần được quan tâm và hỗ trợ thêm.
**2. Nhận xét về kết quả học tập**
Một số sinh viên có kết quả học tập tốt, thể hiện qua điểm số tương đối cao và ổn định ở các thành phần đánh giá. Tiêu biểu là sinh viên SV016 đạt 9,40 điểm, SV004 đạt 9,20 điểm và SV024 đạt 9,00 điểm. Điều này cho thấy các sinh viên này có kết quả tốt trong quá trình học tập và kiểm tra.
Bên cạnh đó, một số sinh viên có điểm tổng kết ở mức trung bình, gần ngưỡng đạt. Những trường hợp này cần tiếp tục củng cố kiến thức, luyện tập thêm các bài thực hành Java và chủ động ôn tập trước các kỳ kiểm tra.
Đáng chú ý, có 5 sinh viên chưa đạt yêu cầu gồm: SV007 (4,50 điểm), SV011 (4,50 điểm), SV017 (4,60 điểm), SV023 (4,90 điểm) và SV027 (4,50 điểm). Trong đó, SV023 có kết quả gần ngưỡng đạt nhất. Các sinh viên này cần được theo dõi và hỗ trợ để cải thiện kết quả học tập.
**3. Đánh giá và đề xuất**
Từ kết quả trên, có thể nhận thấy đa số sinh viên đã hoàn thành yêu cầu của môn học. Tuy nhiên, tỷ lệ 16,67% sinh viên chưa đạt vẫn cần được chú ý.

Giảng viên nên tổ chức các buổi ôn tập, hướng dẫn thêm về kiến thức cơ bản của Java như biến, kiểu dữ liệu, câu lệnh điều kiện, vòng lặp, mảng và lập trình hướng đối tượng. Đối với sinh viên chưa đạt, cần có kế hoạch hỗ trợ phù hợp, khuyến khích làm thêm bài tập thực hành và chủ động hỏi giảng viên khi gặp khó khăn.
Sinh viên cũng cần xây dựng kế hoạch học tập rõ ràng, đi học đầy đủ, hoàn thành bài tập đúng hạn và dành thời gian tự luyện tập sau mỗi buổi học.
 **4. Kết luận**
Nhìn chung, kết quả học tập của lớp tương đối khả quan với tỷ lệ đạt 83,33%. Để nâng cao chất lượng học tập trong thời gian tới, cần duy trì những phương pháp học tập hiệu quả, đồng thời quan tâm hỗ trợ các sinh viên chưa đạt. Mục tiêu là giúp toàn bộ sinh viên nắm vững kiến thức cơ bản và vận dụng được Java vào giải quyết các bài toán thực tế.











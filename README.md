# btvn6
# Bài tập 6: Hệ quản trị CSDL
Chủ đề: Câu lệnh Select
Yêu cầu bài tập: 
Cho file sv_tnut.sql (1.6MB)
1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
6. nhập sql để tìm xem có những sv nào trùng tên với em?
7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
10. HÃY NHẬP SQL ĐỂ LIỆT KÊ CÁC SV NỮ NGÀNH KMT CÓ TRONG BẢNG SV (TRÌNH BÀY QUÁ TRÌNH SUY NGHĨ VÀ GIẢI NHỮNG VỨNG MẮC)

DEADLINE: 23H59:59 NGÀY 25/4/2025

Ghi chú: Giải thích tại sao lại có SQL như vậy.
 #                    Bài làm 
Tạo database mới tên là BT6
![image](https://github.com/user-attachments/assets/0111ab43-5375-4061-ad98-800e4da181c8)
# 1. Hãy nêu các bước để import được dữ liệu trong sv_tnut.sql vào sql server của em
CLICK vào file chọn open rồi chọn file cuối cùng chọn file " sv_tnut " mà e đã tải về
![image](https://github.com/user-attachments/assets/d4516c08-ad81-4879-8b5c-5e70eab7622b)
![image](https://github.com/user-attachments/assets/9f36a70a-d763-4754-8cd1-be7d15a1a66c)
# 2. dữ liệu đầu vào là tên của sv; sđt; ngày, tháng, năm sinh của sinh viên (của sv đang làm bài tập này)
- chọn Execute
![image](https://github.com/user-attachments/assets/71b0d88f-c87d-45b7-956e-fc562d99fd5e)
- Tìm đúng tên bản thân em
![image](https://github.com/user-attachments/assets/0f1479e2-b171-4174-be9c-23f44580a4a5)
# 3. nhập sql để tìm xem có những sv nào trùng hoàn toàn ngày/tháng/năm với em?
![image](https://github.com/user-attachments/assets/b2f412a9-6abc-4948-bfa0-4893885c65f3)
# 4. nhập sql để tìm xem có những sv nào trùng ngày và tháng sinh với em?
![image](https://github.com/user-attachments/assets/bdc511ad-d6de-4fb9-b1b5-3f918c341190)
# 5. nhập sql để tìm xem có những sv nào trùng tháng và năm sinh với em?
![image](https://github.com/user-attachments/assets/9ec97cdb-5aa0-4da6-bf7c-ac87c5a07957)
# 6. nhập sql để tìm xem có những sv nào trùng tên với em?
![image](https://github.com/user-attachments/assets/81a205d5-b076-4aa4-a72a-db7db2f15027)
# 7. nhập sql để tìm xem có những sv nào trùng họ và tên đệm với em.
![image](https://github.com/user-attachments/assets/767ec7ae-ff2d-4fff-928a-40e4a28ded05)
# 8. nhập sql để tìm xem có những sv nào có sđt sai khác chỉ 1 số so với sđt của em.
![image](https://github.com/user-attachments/assets/8a8ed9f8-05e7-402b-b045-db54b254ce5e)
Không có sđt nào sai khác chỉ 1 số so với sđt của em hết
# 9. BẢNG SV CÓ HƠN 9000 ROWS, HÃY LIỆT KÊ TẤT CẢ CÁC SV NGÀNH KMT, SẮP XẾP THEO TÊN VÀ HỌ ĐỆM, KIỂU TIẾNG  VIỆT, GIẢI THÍCH.
![image](https://github.com/user-attachments/assets/32676f9b-fd2d-4cc3-9c1b-bebd8d43cc1c)
- lop LIKE N'%KTP%' or  lop LIKE N'%KMT%' : Tìm tất cả sinh viên thuộc ngành KMT
+ Ở câu lệnh này em thêm lop Like '%KTP%'vào Where vì lớp KMT và KTP là cùng ngành với nhau chỉ khác tên thôi
- ORDER BY ten, hodem : Sắp xếp các tên trước theo vần âm tiết đầu của bảng chữ cái( VD A=>B ), sau đó mới theo họ và tên đệm.
- COLLATE Vietnamese_CI_AS: Đây là kiểu sắp xếp tiếng Việt có phân biệt dấu và chữ hoa/thường hợp lý VD : an => An
# 
![image](https://github.com/user-attachments/assets/f72de6e0-5f81-408c-b964-d9e2e26c9895)
Sau 1 lúc xem xét:
1. Em thấy có 1 số bạn là nam nhưng có tên giống nữ 
2. Vì không có trường giới tính nên sẽ khó nhận biết chính xác được các tên trên có phải là nữ hay không


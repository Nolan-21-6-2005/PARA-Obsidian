# Thuật toán
Vào thông tin sách.
Ra Không có.
1. Tạo node mới.
2. [[Tìm vị trí cần thêm]].
3. Thêm node mới vào sau vị trí đã tìm.
# Pseudo code
Đối tượng `Slist`
Chức năng `AddNode()`
Mô tả:
F là con trỏ đầu để giữ vùng nhớ đầu tiên và truy cập đến các phần tử bên trong.
M là con trỏ trỏ đến vị trí được tìm thấy theo yêu cầu.
```pascal
procedure AddNode(Con_tro F,con_tro M, thong_tin_sach)
	1.{Tao node moi}
	N <= AVAIL
	infor(N) := thong_tin_sach
	link(N) := NULL
	
	if F= NULL then F := N 
	else begin 
		link(N) := link(M); 
		link(M) := N; 
	end;
return
```

Đối tượng `Book`
Chức năng `AddBook()`
```pascal
procedure AddBook (thong_tin_sach, vitri) 
	1{Them thong tin vao node}
	Slist.AddNode(Con_tro_dau, thong_tin_sach, vitri)
return
```

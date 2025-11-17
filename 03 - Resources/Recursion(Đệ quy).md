- Là chia bài toán lớn thành các bài toán nhỏ đồng dạng. 
- Khi giải bài toán chương trình sẽ gọi lời gọi hàm cho đến khi đạt được trạng thái cơ sở thì hàm sẽ dừng lại.

```pascal
Function ThucHien(n) Begin
	If n = 1 begin
		return 1
	end
	
	Else If n = 0 begin
		return 0
	end
	
Return ThucHien(n - 1)	
End
```


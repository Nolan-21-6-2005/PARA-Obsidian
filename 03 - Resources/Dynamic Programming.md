---
tags:
  - Software/Technique
---
> Dynamic Programming = Recursion + Memoization

[[Recursion(Đệ quy)]]: là việc chia nhỏ bài toán ra thành các bài toán con cùng dạng. 

Memoization: Ghi nhớ lại các giá trị khi giải các bài toán con.

```pascal
Function ThucHien(n) Begin
	{luu gia tri phan tu}
	If n <= 1 begin
		return n
	end
Return ThucHien(n - 1)
End
```

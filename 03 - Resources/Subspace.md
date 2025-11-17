Cho tập  
$$ 
W={(x,y,z)\in \mathbb{R}^3 \mid 2x - |y| + 3z = 0}.  
$$ 
Hãy kiểm tra xem (W) có phải **không gian vector con** của $\mathbb{R}^3$ hay không.

---

### Giải dễ hiểu

Để $W$ là **không gian vector con**, nó phải thỏa 2 điều kiện:

1. **Đóng dưới phép nhân vô hướng**:  
    Nếu $v \in W$ thì $c v\in W$ với **mọi** $c \in \mathbb{R}$.
    
2. **Đóng dưới phép cộng**:  
    Nếu $u, v \in W$ thì $u+v \in W$.
    

---

## 1. Kiểm tra nhân vô hướng

Lấy một vector thuộc $W$, ví dụ:  
$$
(1,2,0) \quad\text{vì}\quad 2(1) - |2| + 0 = 2 - 2 = 0.  
$$

Nhân nó với (c = -1):

$$
(-1)(1,2,0)=(-1,-2,0).  
$$

Kiểm tra xem vector mới có còn thuộc (W) không:

$$
2(-1) - |-2| + 0 = -2 - 2 = -4 \neq 0.  
$$

→ **Không còn thuộc (W)**.

Vậy $W$ **không đóng dưới nhân vô hướng** → **không thể** là không gian con.

Lý do: trị tuyệt đối $|y|$ làm thay đổi dấu khi nhân với số âm → không còn tuyến tính.

---

## 2. Kiểm tra phép cộng (cho đầy đủ)

Lấy hai vector đều thỏa điều kiện:

$$
(1,2,0)\in W,\qquad (1,-2,0)\in W.  
$$

Cộng:

$$ 
(1,2,0)+(1,-2,0)=(2,0,0).  
$$

Kiểm tra:

$$
2\cdot 2 - |0| + 0 = 4 \neq 0.  
$$

→ Tổng **không** nằm trong (W).  
Vậy (W) **không đóng dưới phép cộng**.

---

### Kết luận

Do điều kiện chứa **trị tuyệt đối (|y|)**, nên:

- không đóng dưới nhân với mọi số thực,
    
- không đóng dưới phép cộng.
    

Vì vậy:  
$$  
\boxed{W\ \text{không phải không gian vector con của}\ \mathbb{R}^3.}  
$$
---
tags:
  - Math/Caculus
text: Mathematic
---
# 1. Đạo hàm và Vi phân 📈

**Đạo hàm** giúp chúng ta hiểu về tốc độ thay đổi của một hàm số. Nó cho biết hàm số tăng hay giảm nhanh như thế nào tại một điểm cụ thể.

**Định nghĩa Đạo hàm:**  
Đạo hàm của hàm $f(x)$ tại điểm $x_0$ được ký hiệu là $f'(x_0)$ hoặc $\frac{dy}{dx}\bigg|_{x_0}$. Công thức của nó là:

$$
f'(x_0) = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}
$$

**Vi phân của hàm số:**  

$$
dy = f'(x)dx
$$

**Khai triển Taylor:**  

$$
f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \dots + \frac{f^{(n)}(a)}{n!}(x-a)^n + R_n(x)
$$

---

# 2. Tích phân 📊
**Tích phân** là phép toán ngược lại của đạo hàm, giúp tính toán **sự tích lũy** của một đại lượng. Bạn có thể dùng nó để tính diện tích, thể tích, v.v.
**Nguyên hàm và Tích phân bất định:**

$$
\int f(x)dx = F(x) + C
$$

**Tích phân xác định:**  

$$
\int_a^b f(x)dx = F(b) - F(a)
$$

**Công thức tích phân từng phần:**

$$
\int u\,dv = uv - \int v\,du
$$

---

# 3. Hàm nhiều biến 🌐
**Hàm nhiều biến** mô tả mối quan hệ giữa một biến phụ thuộc với nhiều biến độc lập, ví dụ như nhiệt độ phụ thuộc vào cả vĩ độ và kinh độ.
**Đạo hàm riêng:**  

- Đạo hàm riêng theo $x$: $\frac{\partial f}{\partial x}$  
- Đạo hàm riêng theo $y$: $\frac{\partial f}{\partial y}$  

**Vi phân toàn phần:**  

$$
dz = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy
$$

**Tìm cực trị:**  

$$
A = \frac{\partial^2 f}{\partial x^2}, \quad
B = \frac{\partial^2 f}{\partial x \partial y}, \quad
C = \frac{\partial^2 f}{\partial y^2}, \quad
D = AC - B^2
$$

- Nếu $D > 0, A > 0$: cực tiểu  
- Nếu $D > 0, A < 0$: cực đại  
- Nếu $D < 0$: không phải cực trị  

---

# 4. Tích phân kép 🏞️
**Tích phân kép** là tích phân của hàm hai biến, thường dùng để tính thể tích hoặc diện tích.

$$
\iint_D f(x,y) \, dxdy = \iint_{D'} f(r\cos\varphi, r\sin\varphi)\, r\,dr\,d\varphi
$$

với $x = r\cos\varphi, \; y = r\sin\varphi$.


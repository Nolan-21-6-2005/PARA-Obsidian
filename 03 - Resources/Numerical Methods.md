---
tags:
  - Math/NumericalMethods
text: Mathematic
---
# Phương pháp tính

## Chương 1: Số xấp xỉ và Sai số  

### 1. Các khái niệm cơ bản  
- **Số xấp xỉ**: $A \approx a$  
- **Sai số tuyệt đối**: $\Delta = |A-a|$  
- **Sai số tuyệt đối giới hạn**: $A = a \pm \Delta_a$  
- **Sai số tương đối**: $\delta = \dfrac{|A-a|}{|A|}$  
- **Sai số tương đối giới hạn**: $\delta_a = \dfrac{\Delta_a}{|a|}$  

### 2. Sai số của hàm số  
$$
\Delta u \approx \sum_{i=1}^{n} \left| \frac{\partial u}{\partial x_i} \right| \Delta x_i
$$  

- Tổng/Hiệu: $u = x \pm y \;\Rightarrow\; \Delta u = \Delta x + \Delta y$  
- Tích: $u = xy \;\Rightarrow\; \delta_u \approx \delta_x + \delta_y$  
- Thương: $u = \dfrac{x}{y} \;\Rightarrow\; \delta_u \approx \delta_x + \delta_y$  
- Lũy thừa: $u = x^\alpha \;\Rightarrow\; \delta_u \approx |\alpha|\delta_x$

>[!note]
> 

---

## Chương 2: Giải gần đúng phương trình  

### 1. Khoảng phân ly nghiệm  
- $(a,b)$ là khoảng phân ly nghiệm của $f(x)=0$ nếu:  
	1. $f(x)$ liên tục trên $[a,b]$  
	2. $f(a)f(b) < 0$  
	3. $f'(x)$ không đổi dấu trên $(a,b)$  

>[!note]
### 2. Các phương pháp  

**a. Chia đôi**  
$$
b_n - a_n = \frac{b-a}{2^n}, \quad \frac{b-a}{2^n} \leq \varepsilon
$$  

**b. Lặp**  
$$
x_n = \varphi(x_{n-1})
$$  
Điều kiện hội tụ: $|\varphi'(x)| \leq q < 1$  
Sai số:  
$$
|x_n - \xi| \leq \frac{q^n}{1-q}|x_1 - x_0|
$$  

**c. Dây cung**  
$$
x_{n+1} = \frac{x_n f(d) - d f(x_n)}{f(d) - f(x_n)}
$$  
Sai số:  
$$
|x_n - \xi| \leq \frac{|f(x_n)|}{m_1}, \quad m_1 = \min |f'(x)|
$$  
> [!note]

---

## Chương 3: Giải gần đúng hệ phương trình tuyến tính  

### 1. Chuẩn và hội tụ  
$$
\|A\|_\infty = \max_i \sum_{j=1}^{n} |a_{ij}|
$$  
$$
\lim_{k\to\infty} \|x^{(k)} - x^*\| = 0
$$  
> [!note]
> 
### 2. Các phương pháp lặp  

- **Jacobi**  
$$
x^{(k+1)} = \beta + \alpha x^{(k)}
$$  
- Sai số:  
$$
\|x^{(k)} - x^*\|_\infty \leq \frac{\|\alpha\|_\infty^k}{1-\|\alpha\|_\infty}\|x^{(1)} - x^{(0)}\|_\infty
$$  

- **Seidel (Gauss–Seidel)**  
$$
x_i^{(k+1)} = \beta_i + \sum_{j=1}^{i-1}\alpha_{ij}x_j^{(k+1)} + \sum_{j=i+1}^{n}\alpha_{ij}x_j^{(k)}
$$  
>[!note]

---

## Chương 4: Nội suy & Bình phương bé nhất  

### 1. Nội suy  

- **Lagrange**  
$$
P_n(x) = \sum_{i=0}^{n} y_i L_i(x), \quad L_i(x) = \prod_{k=0, k\neq i}^{n} \frac{x - x_k}{x_i - x_k}
$$  

- **Newton**  
$$
P_n(x) = y_0 + f[x_0,x_1](x-x_0) + \dots + f[x_0,\dots,x_n](x-x_0)\dots(x-x_{n-1})
$$
>[!note]

### 2. Bình phương bé nhất  
$$
S = \sum_{i=1}^{n} (y_i - g(x_i))^2
$$  

Với $g(x)=a+bx$:  
$$
\begin{cases}
na + b\sum x_i = \sum y_i \\
a\sum x_i + b\sum x_i^2 = \sum x_i y_i
\end{cases}
$$  
> [!note]

---

## Chương 5: Gần đúng Đạo hàm và Tích phân  

### 1. Đạo hàm gần đúng  
- Sai phân tiến:  
$$
f'(x_i) \approx \frac{y_{i+1} - y_i}{x_{i+1}-x_i}
$$  

- Sai phân lùi:  
$$
f'(x_i) \approx \frac{y_i - y_{i-1}}{x_i - x_{i-1}}
$$  

### 2. Tích phân gần đúng  

- **Công thức hình thang**  
$$
I \approx \frac{h}{2} \Big[ y_0 + y_n + 2\sum_{i=1}^{n-1} y_i \Big], \quad h=\frac{b-a}{n}
$$  

- **Công thức Simpson**  
$$
I \approx \frac{h}{3} \Big[ y_0 + y_{2m} + 4\sum_{i=1}^{m} y_{2i-1} + 2\sum_{i=1}^{m-1} y_{2i} \Big]
$$  

---

## Chương 6: Giải gần đúng phương trình vi phân  

### 1. Bài toán Cauchy  
- Dạng 1:  
$$
\begin{cases}
y' = f(x,y) \\
y(x_0) = \alpha
\end{cases}
$$  

- Dạng 2:  
$$
\begin{cases}
y' = f_1(x,y,z) \\
z' = f_2(x,y,z) \\
y(x_0) = \alpha_1, \; z(x_0) = \alpha_2
\end{cases}
$$  

### 2. Euler  
$$
\begin{cases}
y_0 = \alpha \\
y_{i+1} = y_i + h f(x_i,y_i)
\end{cases}
$$  

### 3. Chuỗi Taylor  
$$
y(x) \approx y(x_0) + y'(x_0)(x-x_0) + \frac{y''(x_0)}{2!}(x-x_0)^2 + \dots + \frac{y^{(k)}(x_0)}{k!}(x-x_0)^k
$$  

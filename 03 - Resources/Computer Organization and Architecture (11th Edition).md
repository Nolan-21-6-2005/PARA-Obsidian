---
tags:
  - Reference
---

## **Phần 1: Giới thiệu**

- **Máy tính = phần cứng + kiến trúc + tổ chức.**
    
- _Kiến trúc (architecture)_: những gì lập trình viên thấy (tập lệnh, thanh ghi, bộ nhớ).
    
- _Tổ chức (organization)_: cách phần cứng thực hiện (mạch, điều khiển, bus).
    
- **Nguyên lý von Neumann**: chương trình và dữ liệu lưu chung trong bộ nhớ, CPU đọc từng lệnh để thực thi.
    

👉 Hiểu đơn giản: kiến trúc là “thiết kế trên giấy”, tổ chức là “cách lắp ráp thực tế”.

---

## **Phần 2: Máy tính và hệ thống xử lý**

- **Bộ xử lý trung tâm (CPU)**: gồm ALU (tính toán), CU (điều khiển), thanh ghi (lưu tạm).
    
- **Chu kỳ lệnh**: _fetch → decode → execute_.
    
- **Pipeline**: chia nhỏ công việc, nhiều lệnh xử lý song song.
    
- **Superscalar**: nhiều pipeline chạy cùng lúc.
    

👉 Giống như dây chuyền sản xuất: chia việc để nhanh hơn.

---

## **Phần 3: Bộ nhớ**

- **Phân cấp bộ nhớ**:
    
    - Thanh ghi → Cache → RAM → Ổ cứng.
        
    - Nhanh thì nhỏ và đắt, chậm thì rẻ và lớn.
        
- **Cache**: bộ nhớ nhỏ, rất nhanh, lưu dữ liệu thường dùng.
    
- **Nguyên tắc Locality**: chương trình hay lặp lại dữ liệu gần nhau, cache tận dụng điều này.
    

👉 Cache như sổ tay để ghi nhanh thay vì tra cứu cả thư viện.

---

## **Phần 4: Input/Output (I/O)**

- Thiết bị vào/ra giao tiếp qua **I/O modules**.
    
- **Kỹ thuật điều khiển I/O**:
    
    - Polling: CPU hỏi liên tục.
        
    - Interrupt: thiết bị báo ngược cho CPU.
        
    - DMA (Direct Memory Access): thiết bị truy cập thẳng RAM, không cần CPU can thiệp.
        

👉 Giống như: tự đi lấy (polling), được gọi khi có việc (interrupt), hay nhờ người khác lấy hộ (DMA).

---

## **Phần 5: Instruction Sets (Tập lệnh)**

- **CISC (Complex Instruction Set Computer)**: nhiều lệnh phức tạp, dễ lập trình, CPU phức tạp.
    
- **RISC (Reduced Instruction Set Computer)**: ít lệnh, đơn giản, thực thi nhanh.
    
- **Định dạng lệnh**: opcode (loại lệnh) + toán hạng (dữ liệu/địa chỉ).
    

👉 RISC giống công cụ đơn giản nhưng hiệu quả, CISC giống dao đa năng nhưng cồng kềnh.

---

## **Phần 6: Kiến trúc song song**

- **Multiprocessing**: nhiều CPU thật sự.
    
- **Multithreading**: nhiều luồng chạy trên cùng CPU.
    
- **MIMD / SIMD** (Flynn’s taxonomy): nhiều dữ liệu và nhiều lệnh song song.
    

👉 Ví dụ: nhiều công nhân (CPU) cùng làm, hoặc 1 công nhân xử lý nhiều phần việc nhỏ song song (multithreading).

---

## **Phần 7: Điều khiển và vi điều khiển**

- **Hardwired control**: mạch cố định, nhanh nhưng khó sửa.
    
- **Microprogrammed control**: dùng bộ nhớ lưu vi lệnh, dễ thay đổi nhưng chậm hơn.
    

👉 Giống như luật khắc vào đá (hardwired) vs viết vào sổ tay (microprogrammed).

---

## **Phần 8: Bộ xử lý nâng cao**

- **Speculative execution**: dự đoán nhánh, thực thi trước.
    
- **Out-of-order execution**: chạy lệnh không cần đúng thứ tự nếu không phụ thuộc dữ liệu.
    
- **Branch prediction**: đoán hướng rẽ nhánh để CPU không phải chờ.
    

👉 Giống như đoán trước để tiết kiệm thời gian, dù có thể đoán sai.

---

## **Phần 9: Hiệu năng**

- **Thước đo**: CPI (chu kỳ/lệnh), MIPS, FLOPS.
    
- **Amdahl’s Law**: tăng tốc một phần thì toàn hệ thống chỉ nhanh hơn giới hạn nhất định.
    
- **Benchmarking**: dùng chương trình chuẩn để đo hiệu năng.
    

👉 Giống như cải thiện 1 đoạn đường nhưng tổng thời gian đi vẫn phụ thuộc các đoạn khác.

---

## **Phần 10: Bộ nhớ ảo và hệ điều hành**

- **Virtual memory**: giả lập bộ nhớ lớn hơn RAM thật bằng cách hoán đổi với ổ cứng.
    
- **Paging**: chia bộ nhớ thành khối nhỏ, dễ quản lý.
    
- **TLB (Translation Lookaside Buffer)**: cache cho địa chỉ ảo → vật lý.
    

👉 Giống như dùng thêm kho thuê ngoài khi nhà chật.

---

## **Tóm lại**

Sách dạy:

1. Cấu trúc CPU, bộ nhớ, I/O.
    
2. Tập lệnh và cách lập trình máy thấp cấp.
    
3. Các kỹ thuật tăng tốc: pipeline, superscalar, branch prediction.
    
4. Hệ thống song song: nhiều CPU, nhiều luồng.
    
5. Nguyên lý quản lý bộ nhớ và ảo hóa.
    
6. Thước đo hiệu năng và tối ưu hóa.
    
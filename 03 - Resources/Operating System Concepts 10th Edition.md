---
tags:
  - Books
text: Books
---
# **Phần I – Tổng quan**

### **Chương 1: Giới thiệu**

- OS = phần mềm trung gian giữa user ↔ phần cứng.
    
- Mục tiêu: tiện dụng + hiệu quả.
    
- Tài nguyên quản lý: CPU, bộ nhớ, thiết bị I/O, file.
    
- Hệ thống: batch, time-sharing, multiprogramming, personal OS, distributed, real-time.  
    👉 Hiểu đơn giản: OS là “người quản lý công việc” cho máy tính.
    

### **Chương 2: Cấu trúc hệ điều hành**

- Các kiểu tổ chức:
    
    - **Monolithic**: 1 khối lớn.
        
    - **Layered**: chia tầng (hardware → OS → apps).
        
    - **Microkernel**: nhân nhỏ, dịch vụ user-level.
        
    - **Modules**: dạng plug-in.
        
    - **Hybrid**: mix.  
        👉 Giống cách tổ chức công ty: tập trung 1 nơi, phân tầng, hay chia module.
        

---

# **Phần II – Tiến trình & Lập lịch**

### **Chương 3: Tiến trình**

- **Process** = chương trình đang chạy.
    
- Gồm code, data, stack, heap.
    
- **PCB (Process Control Block)**: hồ sơ trạng thái.
    
- **Context switch**: đổi CPU cho process khác.  
    👉 Giống như nhiều việc song song, hồ sơ giúp tiếp tục đúng chỗ.
    

### **Chương 4: Luồng & đa luồng**

- **Thread**: đơn vị thực thi trong process.
    
- Ưu điểm: nhẹ, chia sẻ tài nguyên.
    
- **Multithreading**: cải thiện hiệu suất, responsiveness.
    
- **User-level vs Kernel-level threads**.  
    👉 Như nhóm cùng làm dự án, chia việc nhỏ.
    

### **Chương 5: Lập lịch CPU**

- Mục tiêu: tối ưu throughput, turnaround, waiting time, response.
    
- Thuật toán:
    
    - FCFS
        
    - SJF
        
    - RR
        
    - Priority
        
    - Multilevel queue
        
    - Multilevel feedback queue  
        👉 Giống xếp hàng: theo lượt, ưu tiên, hoặc chia lớp.
        

---

# **Phần III – Đồng bộ hóa & Deadlock**

### **Chương 6: Đồng bộ hóa tiến trình**

- **Race condition**: nhiều tiến trình tranh tài nguyên.
    
- **Critical section**: đoạn cần khóa.
    
- Giải pháp:
    
    - Peterson’s algorithm
        
    - Mutex
        
    - Semaphore (binary, counting)
        
    - Monitors  
        👉 Giống WC chỉ cho 1 người vào.
        

### **Chương 7: Deadlock**

- **Deadlock** = tiến trình chờ nhau vô hạn.
    
- Điều kiện (Coffman): Mutual exclusion, Hold&Wait, No preemption, Circular wait.
    
- Xử lý: phòng tránh, ngăn chặn, phát hiện, hồi phục.
    
- Thuật toán: Banker's algorithm.  
    👉 Như tắc đường vòng tròn.
    

---

# **Phần IV – Quản lý bộ nhớ**

### **Chương 8: Bộ nhớ chính**

- **Mục tiêu**: hiệu quả + bảo vệ.
    
- Kỹ thuật:
    
    - Swapping
        
    - Fixed / variable partitioning
        
    - Paging: page ↔ frame
        
    - Segmentation: chia theo logic  
        👉 Paging như chia thành trang sách, segmentation như chia thành chương.
        

### **Chương 9: Bộ nhớ ảo**

- Khái niệm: không gian nhớ ảo lớn hơn RAM thật.
    
- **Demand paging**: chỉ nạp khi cần.
    
- **Page replacement**: FIFO, LRU, Optimal.
    
- **Thrashing**: quá tải swap.  
    👉 Giống mượn sách từ thư viện khi cần.
    

---

# **Phần V – Quản lý lưu trữ**

### **Chương 10: Hệ thống file**

- File = tập dữ liệu có tên.
    
- Directory = chứa file.
    
- Operations: tạo, xóa, đọc, ghi, seek.
    
- File attributes (size, type, owner).  
    👉 Giống hồ sơ tài liệu.
    

### **Chương 11: Cài đặt hệ thống file**

- Cách lưu file:
    
    - Contiguous
        
    - Linked
        
    - Indexed
        
- FAT, inode.
    
- Free space management: bitmap, linked list.  
    👉 Giống sắp xếp sách: liền nhau, nối bằng chỉ mục.
    

### **Chương 12: Lưu trữ khối (Secondary Storage)**

- Ổ đĩa: cylinder, track, sector.
    
- Scheduling: FCFS, SSTF, SCAN, C-SCAN.
    
- RAID: 0,1,5,… tăng tốc/độ tin cậy.  
    👉 Giống robot lấy đĩa CD, tối ưu đường đi.
    

### **Chương 13: Input/Output**

- Cơ chế: polling, interrupt, DMA.
    
- Buffering, caching, spooling.
    
- Device drivers.  
    👉 Giống thư ký xử lý giấy tờ hộ sếp.
    

---

# **Phần VI – Bảo mật & An toàn**

### **Chương 14: Bảo mật hệ điều hành**

- Nguyên tắc: xác thực (authentication), phân quyền (authorization).
    
- Mô hình: Access Matrix, ACL, Capabilities.  
    👉 Như thẻ ra vào công ty.
    

### **Chương 15: An toàn hệ thống**

- Nguy cơ: virus, worm, trojan, rootkit.
    
- Biện pháp: firewall, IDS, mã hóa, backup.
    
- Policy: least privilege, defense-in-depth.  
    👉 Giống bệnh truyền nhiễm → cần vaccine, kiểm dịch.
    

---

# **Phần VII – Hệ thống nâng cao**

### **Chương 16: Hệ điều hành phân tán**

- Tài nguyên nhiều máy dùng chung.
    
- Transparency: truy cập như 1 hệ.
    
- Distributed file system, synchronization, election algorithm.  
    👉 Giống nhiều chi nhánh như 1 văn phòng.
    

### **Chương 17: Virtualization & Cloud**

- Virtual machine monitor (hypervisor).
    
- Type 1 (bare-metal), Type 2 (hosted).
    
- Cloud models: IaaS, PaaS, SaaS.  
    👉 Giống chia 1 căn nhà thành nhiều phòng cho thuê.
    

### **Chương 18: Multiprocessor & Multicore**

- Symmetric vs Asymmetric multiprocessing.
    
- Multicore = nhiều CPU trên 1 chip.
    
- Challenges: cache coherence, synchronization.  
    👉 Giống nhiều đầu bếp trong 1 bếp.
    

---

# **Phần VIII – Case Studies**

### **Chương 19: Linux**

- Kiến trúc: monolithic + module.
    
- Process & thread management: fork(), exec().
    
- File system: ext4.
    
- Memory management: demand paging, swapping.  
    👉 Phổ biến server, mobile (Android).
    

### **Chương 20: Windows 10**

- Kiến trúc: layered + microkernel hybrid.
    
- Windows API, subsystems.
    
- NTFS file system.
    
- Security: Active Directory, ACL.  
    👉 Phổ biến PC, doanh nghiệp.
    

---

# **Phụ lục**

- Cấu trúc máy tính cơ bản (CPU, I/O).
    
- Mô hình toán học: queuing, Petri nets.
    
- Lý thuyết song song.
    

---

📌 **Tóm tắt tổng thể**

1. OS quản lý: CPU, bộ nhớ, file, I/O.
    
2. Quản lý tiến trình: process, thread, scheduling, sync, deadlock.
    
3. Quản lý bộ nhớ: paging, segmentation, virtual memory.
    
4. Quản lý lưu trữ: file system, disk, RAID, I/O.
    
5. An toàn & bảo mật: access control, malware, defense.
    
6. Hệ thống nâng cao: distributed, virtualization, multicore.
    
7. Case study: Linux, Windows.
    

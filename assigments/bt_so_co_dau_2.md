# 📝 Bài tập: Biểu diễn số có dấu, phép toán và tràn số

---

## Bài 1. Biểu diễn số có dấu (8 bit)
Cho số **-23**.  
1. Biểu diễn ở các dạng:  
   - Dấu–độ lớn (Sign–Magnitude).  
   - Bù 1 (One’s Complement).  
   - Bù 2 (Two’s Complement).  
2. Đổi ngược về số thập phân để kiểm tra tính đúng đắn.  

---

## Bài 2. Phép cộng số có dấu (4 bit, bù 2)  
Cho hai số nhị phân 4 bit dạng bù 2:  
- A = 1101  
- B = 0101  

1. Đổi ra số thập phân.  
2. Thực hiện phép cộng trên nhị phân.  
3. Kiểm tra kết quả bằng cách so sánh với phép cộng thập phân.  

---

## Bài 3. Phép trừ số có dấu (8 bit, bù 2)  
Cho hai số thập phân: **45 – 78**.  

1. Biểu diễn cả hai số trên 8 bit dạng bù 2.  
2. Thực hiện phép trừ bằng cách cộng với số đối.  
3. Đổi kết quả ra thập phân và so sánh.  

---

## Bài 4. Kiểm tra tràn số (Overflow)  
Cho hai số nguyên 8 bit ở dạng bù 2:  
- A = 01100110 (102)  
- B = 01101011 (107)  

1. Thực hiện phép cộng A + B.  
2. Cho biết kết quả nhị phân và thập phân.  
3. Có xảy ra tràn số không? Giải thích dựa trên dấu và bit nhớ.  

---

## Bài 5. Bài tập tổng hợp  
1. Biểu diễn số **-128** và **127** trong 8 bit bù 2.  
2. Thực hiện phép cộng sau (8 bit bù 2):  
   - a) 01111111 + 00000001  
   - b) 10000000 + 11111111  
3. Xác định xem các phép toán trên có gây tràn số không, và giải thích.  

---

# ➕ Biểu diễn số có dấu

## Các cách biểu diễn (n bit)
- **Sign–Magnitude (Dấu–Độ lớn)**  
  - Bit MSB = dấu (0:+, 1:–)  
  - Trị tuyệt đối lưu trong (n–1) bit còn lại  
  - Nhược điểm: có 2 số 0 ( +0 và –0 )  

- **One’s Complement (Bù 1)**  
  - Số âm = đảo bit số dương tương ứng  
  - Nhược điểm: vẫn có 2 số 0  

- **Two’s Complement (Bù 2)**  
  - Số âm = đảo bit rồi +1  
  - Ưu điểm: chỉ có 1 số 0, dễ thực hiện phép toán  
  - Được dùng phổ biến trong máy tính hiện nay  

---

# 🧮 Phép toán số có dấu

- **Cộng/Trừ**: thực hiện như số nhị phân không dấu  
  - Nếu dùng bù 2 thì cộng/trừ thống nhất  
  - Trừ: A – B = A + (–B)  

- **Ví dụ (4 bit bù 2):**  
# 🔢 Biểu diễn số thực

## 1. Fixed-Point (Số thực cố định)
- Phần nguyên & phần thập phân được biểu diễn trên số bit cố định  
- Đơn giản, tính toán nhanh  
- Nhược điểm: **phạm vi hẹp, độ chính xác thấp**  
- Thường dùng trong **hệ thống nhúng, DSP đơn giản**

---

## 2. Floating-Point (Số thực dấu phẩy động)
- Dựa trên chuẩn **IEEE 754**  
- Biểu diễn:  
± 1.mantissa × 2^(exponent)
- **Ưu điểm:**  
- Biểu diễn phạm vi rất rộng  
- Có độ chính xác cao  
- **Nhược điểm:**  
- Tính toán phức tạp, tốn tài nguyên phần cứng  
- Dùng trong **khoa học, AI, đồ họa, tính toán chính xác cao**


# ⚠️ Tràn số & Exception

## Tràn số nguyên (Integer Overflow)
- Xảy ra khi kết quả vượt tầm biểu diễn:  
  Min = –2^(n–1), Max = 2^(n–1)–1  
- **Máy tính thực tế:**  
  - CPU chỉ bật **cờ tràn (OF – Overflow Flag)**  
  - Kết quả tính toán theo modulo 2^n → **không tự sinh exception**  
  - Ví dụ (8 bit, bù 2):  
    ```
    01111111 (127) + 00000001 (1) = 10000000 (–128)
    ```

## Tràn số thực (Floating Point Overflow)
- Khi kết quả vượt chuẩn IEEE-754  
- Có thể sinh:  
  - **Exception** (Floating Point Exception)  
  - Hoặc giá trị đặc biệt: **+∞, –∞, NaN**

## Ngôn ngữ lập trình
- **C/C++/Java:** không báo lỗi, kết quả wrap-around  
- **Python, Ada, Rust (checked mode):** có thể sinh lỗi runtime  

👉 Kết luận: Tràn số nguyên **thường không gây exception**,  
chỉ có số thực mới dễ sinh lỗi hoặc giá trị đặc biệt.


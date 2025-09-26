# 📝 Bài tập: Chuyển đổi giữa các hệ số

---

## Bài 1. Thập phân → Nhị phân  
Chuyển các số thập phân sau sang **nhị phân (base 2)** trên 8 bit:  
1. 25  
2. 100  
3. 255  

---

## Bài 2. Nhị phân → Thập phân  
Chuyển các số nhị phân sau sang **thập phân (base 10)**:  
1. 101011  
2. 11111111  
3. 10011001  

---

## Bài 3. Thập phân ↔ Bát phân  
1. Đổi số thập phân **345** sang bát phân (base 8).  
2. Đổi số bát phân **765** sang thập phân.  

---

## Bài 4. Thập phân ↔ Thập lục phân  
1. Chuyển số thập phân **2025** sang thập lục phân (hex).  
2. Chuyển số hex **0x3F2** sang thập phân.  

---

## Bài 5. Kết hợp nhiều hệ  
1. Chuyển số nhị phân **110101101** sang:  
   - Thập phân  
   - Bát phân  
   - Thập lục phân  
2. Chuyển số hex **0x7B** sang nhị phân và thập phân.  

---

# Lý thuyết 
# 🔢 Chuyển đổi giữa các hệ số (Slide 1)

## Các hệ số phổ biến
- **Nhị phân (Binary, base 2):** 0, 1  
- **Bát phân (Octal, base 8):** 0–7  
- **Thập phân (Decimal, base 10):** 0–9  
- **Thập lục phân (Hexadecimal, base 16):** 0–9, A–F  

## Nguyên tắc chuyển đổi
- **Thập phân → hệ khác:** chia liên tiếp cho cơ số, lấy phần dư.  
- **Hệ khác → thập phân:** nhân trọng số (cơ số^vị trí).  
- **Giữa các hệ 2, 8, 16:** gom nhóm bit (3 bit ↔ Octal, 4 bit ↔ Hex).  

---
# 📊 Bảng quy đổi nhị phân sang Octal (gom 3 bit)

| Nhị phân (3 bit) | Bát phân (Octal) |
|------------------|------------------|
| 000              | 0                |
| 001              | 1                |
| 010              | 2                |
| 011              | 3                |
| 100              | 4                |
| 101              | 5                |
| 110              | 6                |
| 111              | 7                |

---

# 📊 Bảng quy đổi nhị phân sang Hex (gom 4 bit)

| Nhị phân (4 bit) | Hexadecimal (Hex) |
|------------------|-------------------|
| 0000             | 0                 |
| 0001             | 1                 |
| 0010             | 2                 |
| 0011             | 3                 |
| 0100             | 4                 |
| 0101             | 5                 |
| 0110             | 6                 |
| 0111             | 7                 |
| 1000             | 8                 |
| 1001             | 9                 |
| 1010             | A                 |
| 1011             | B                 |
| 1100             | C                 |
| 1101             | D                 |
| 1110             | E                 |
| 1111             | F                 |


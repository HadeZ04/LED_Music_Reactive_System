# Hệ Thống LED Phản Ứng Theo Âm Thanh 🎵 (STM32 + Mạch Analog + LED Đơn)

Dự án này sử dụng **vi điều khiển STM32 (Blue Pill)** kết hợp với **mạch khuếch đại âm thanh analog (LM386)** và các **LED đơn** để hiển thị hiệu ứng ánh sáng dựa trên cường độ âm thanh môi trường.
## 📸 Sơ Đồ Mạch


![Sơ đồ mạch LED](![Untitled](https://github.com/user-attachments/assets/04781e05-b46b-43a5-94ab-37188c76b5be))

## ⚙️ Thành Phần Phần Cứng

| Thành phần       | Mô tả |
|------------------|-------|
| STM32 Blue Pill  | Vi điều khiển chính |
| LM386            | IC khuếch đại âm thanh |
| MK1              | Micro điện dung |
| LED x15          | LED 5mm thường |
| Các tụ, điện trở | Lọc nhiễu, định thiên, bảo vệ tín hiệu |
| Biến trở 10k     | Điều chỉnh độ nhạy âm thanh |
| Nguồn 5V/3.3V    | Cấp nguồn cho mạch |

## 🔌 Nguyên Lý Hoạt Động

1. Micro **MK1** thu tín hiệu âm thanh → khuếch đại bởi IC **LM386**.
2. Tín hiệu tương tự (analog) được đưa vào chân **PA2 (ADC)** của STM32.
3. STM32 sử dụng **ADC** để đọc biên độ tín hiệu.
4. Dựa trên cường độ tín hiệu, **từ 1 đến 15 LED** được bật tương ứng.
   - Âm thanh càng lớn → càng nhiều LED sáng.
5. Tốc độ quét nhanh tạo cảm giác LED "nhảy" theo nhạc.

## 🔋 Sơ Đồ Kết Nối LED

| LED   | GPIO STM32 |
|--------|-------------|
| LED1   | PB12        |
| LED2   | PB13        |
| LED3   | PB14        |
| LED4   | PA8         |
| LED5   | PA9         |
| LED6   | PA10        |
| LED7   | PA11        |
| LED8   | PA12        |
| LED9   | PA15        |
| LED10  | PB3         |
| LED11  | PB4         |
| LED12  | PB5         |
| LED13  | PB6         |
| LED14  | PB7         |
| LED15  | PB8         |



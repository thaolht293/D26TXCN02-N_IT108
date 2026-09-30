# D26TXCN02-N_IT108_Session2_Ex01
# Phân tích tốc độ Internet 
## 1. Phân tích lỗi và sửa lời giải 
Nhầm Mbps với MB/s  
Gói mạng 100 Mbps tương đương 100 MB/s. 
**Sai.** 
Mbps là megabit trên giây, còn MB/s là megabyte trên giây. 
Theo công thức: 
 1 Byte = 8 Bits 
thì
100 Mbps / 8 = 12,5 MB/s 
Vậy gói mạng 100 Mbps có tốc độ tải lý thuyết khoảng 12,5 MB/s. 
### Lỗi cho rằng nhà mạng chỉ cung cấp 12,5% tốc độ cam kết
Trình duyệt chỉ hiển thị 12,5 MB/s nên nhà mạng chỉ cung cấp 12,5% tốc độ cam kết. 
**Sai.** 
Tốc độ trình duyệt hiển thị là: 
12,5 MB/s  
Đổi sang Mbps:  
12,5 x 8 = 100 Mbps 
12,5 MB/s thực chất tương đương 100 Mbps. 
Tốc độ tải 12,5 MB/s phù hợp với tốc độ lý thuyết của gói mạng 100 Mbps.  
### Lỗi tính sai thời gian tải tệp 1 GB khi mạng 40 Mbps* 
Mạng 40 Mbps tải tệp 1 GB mất khoảng 25 giây. 
**Sai.** 
Đầu tiên đổi tốc độ:  
40 Mbps / 8 = 5 MB/s 
Với quy ước:  
1 GB = 1.000 MB  
Thời gian tải:  
1.000 / 5 = 200 giây  
Đổi sang phút:  
200 giây = 3 phút 20 giây  
Vậy tệp 1 GB sẽ mất khoảng 200 giây, tương đương 3 phút 20 giây trong điều kiện lý tưởng. 
## 2. Kết luận  
Nguyên nhân của các lỗi trên là do nhầm lẫn giữa **Bit** và **Byte**.  
Tóm lại: 
100 Mbps = 12,5 MB/s 
12,5 MB/s = 100 Mbps 
40 Mbps = 5 MB/s 
Tệp 1 GB ở tốc độ 40 Mbps mất khoảng 200 giây  
bạn Nam **không nên khiếu nại nhà mạng chỉ dựa trên việc trình duyệt hiển** 

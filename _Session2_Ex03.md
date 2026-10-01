# D26TXCN02-N_IT108_Session2_Ex03
## Mục tiêu

> **Phân tích sự phối hợp giữa CPU, RAM và Storage trong mô hình IPO**
> 
> **Đề xuất giải pháp xử lý khi hệ thống quá tải dựa trên Task Manager**

## Yêu cầu nghiệp vụ

### Tình trạng máy
Máy tính đang chạy 30 tab Chrome để làm bài tập. Hệ thống bắt đầu có hiện tượng "giật lag", chuột di chuyển không mượt.
+ Mỗi một tab chorme đều chiếm dung lượng RAM, mở một lượt 30 tab dẫn đến RAM đầy.
+ Khi dung lượng RAM đã hết, hệ điều hành (os) bắt đầu sử dụng bộ nhớ ảo thông qua kỹ thuật Swap file/ Page file từ RAM sang ổ cứng.
### Phân tích kỹ thuật "Swap/Page File" (dùng ổ cứng thay RAM) và tác động của nó đến hiệu năng
Khi RAM đầy, OS chọn các dữ liệu ít truy cập hoặc đã lâu chưa truy cập (vd: các tab Chrome đang chạy ngầm) và ghi tạm xuống tệp pagefile trên ổ cứng để lấy chỗ cho trình đang chạy. Khi cần dùng lại tab đó, dữ liệu lại được swap ngược lại RAM (Page In/Page Out). Tốc độ của ổ cứng ngay cả SSD chậm hơn RAM hàng chục đến hàng trăm lần. NẾu liên tục chuyển dữ liệu qua lại giữa RAM và ổ cứng gây ra hiện tượng Thrashing nghẽn cổ chai I/O ==> máy bị khựng, chuột di chuyển không mượt và giật lag nặng.

## Kiểm thử

 ### Hệ thống đang dùng ổ cứng HDD truyền thống. Điều gì xảy ra so với nếu máy dùng ổ SSD NVMe trong tình huống này???
 Như đã giải thích như trên dù cho có sử dụng SSD thì vẫn sẽ chậm hơn RAM. Nếu HDD máy sẽ gần như là xịt keo đóng băng thì với SSD thì máy vẫn phản hồi tương đối mượt NHƯNG VẪN CHẬM HƠN RAM. IloveRAM

 ## Yêu cầu đầu ra

 ### Phân tích và giải pháp
``` mermaid
graph TD;
    subgraph INPUT ["INPUT"]
        A[Gõ Tìm kiếm gì đó <br> Click vào ] 
    end
    subgraph PROCESS ["PROCESS"]
        B[CPU: Xử lý html/js]
        C[RAM: Lưu trữ tab đang dùng]
        D[Page file: Lưu tab ngầm <br> Khi RAM bị tràn]
    end
    subgraph OUTPUT ["OUTPUT"]
        E[Màn hình: hiển thị thứ đang web đang tìm]
        F[Loa: âm thanh quảng cáo]
    end
A --> B;
B --> C;
C -- Tràn RAM --> D;
B --> E;
B --> F;

```



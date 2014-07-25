command-tcpdump
===============

Giải thích về lệnh tcpdump trong linux

### Giới thiệu về TCPDUMP

TCPDUMP là công cụ dùng để "thăm dò (đánh hơi)" các gói tin trong mạng (packet sniffer) bằng cách sử dụng lệnh tcpdump trong các distro linux. 
<br>
Lệnh tcmdump là công cụ thăm dò và phân tích các gói tin trong một hệ thống mạng LAB. Các gói tin này được thu thập hoặc được lọc từ các gói tin trong bộ giao thức TCP/IP, các gói tin này được nhận hoặc truyền trong hệ thống mạng thông qua một card mạng cụ thể của máy tính.

Kết quả của lệnh tcpdump được lưu với đuôi là pcap, file này có thể mở bằng công cụ đồ họa wireshark.

### Cài đặt 
- `tcpdump` thường sẽ có sẵn trong các distro ubuntu, centos ...(linux). Nếu chưa có thực hiện lệnh dưới để cài đặt

> Đối với CENTOS : `yum install tcpdump -y`
> Đối với UBUNTU : `apt-get install tcmdump -y`








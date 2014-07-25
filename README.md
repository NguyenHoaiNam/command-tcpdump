command-tcpdump
===============

Giải thích về lệnh tcpdump trong linux

### Giới thiệu về TCPDUMP

TCPDUMP là công cụ dùng để "thăm dò (đánh hơi)" các gói tin trong mạng (packet sniffer) bằng cách sử dụng lệnh tcpdump trong các distro linux. 
<br>
Lệnh tcpdump là công cụ thăm dò và phân tích các gói tin trong một hệ thống mạng LAB. Các gói tin này được thu thập hoặc được lọc từ các gói tin trong bộ giao thức TCP/IP, các gói tin này được nhận hoặc truyền trong hệ thống mạng thông qua một card mạng cụ thể của máy tính.

Kết quả của lệnh tcpdump được lưu với đuôi là pcap, file này có thể mở bằng công cụ đồ họa wireshark.

### Cài đặt 
- `tcpdump` thường sẽ có sẵn trong các distro ubuntu, centos ...(linux). Nếu chưa có thực hiện lệnh dưới để cài đặt:

```
Đối với CENTOS : yum install tcpdump -y
Đối với UBUNTU : apt-get install tcmdump -y
```
### Các ví dụ sử dụng với tcpdump
#### Thu thập các gói tin từ card mạng cụ thể
```sh
tcpdump -i eth0
```
Lệnh trên trên sẽ thu thập các gói tin đi qua card mạng có tên là eth0, nhờ tùy chọn  `-i`.

#### Thu thập số gói tin chỉ định (ví dụ 9 gói)
```sh
tcpdump -c 9 -i eth0
```
- Tùy chọn `-c 9` sẽ chỉ thị rằng tcpdump sẽ thu thập 9 gói tin đầu tiên khi bắt đầu thực hiện lệnh trên card eth0. 

#### Thu thập và lưu dữ liệu thu thập thành file
- Thông thường kết quả của lệnh tcpdump sẽ hiển thi ra màn hình, nếu muốn lưu kết quả này thành file để đọc bởi các chương trình đồ họa (Wireshark) ta thêm thông số `-w` khi thực thi lệnh.
```sh
tcpdump -w dulieuthuthap.pcap -i eth0
```

#### Đọc file `pcap` bằng tcpdump
```sh
tcpdump -r dulieuthuthap.pcap
```
#### Thu thập dữ liệu bằng địa chỉ IP của card mạng.
- Thông thường khi thu thập dữ liệu, trên màn hình sẽ hiển thị hostname của máy, nếu muốn hiển thị `ip address` ta sử dụng tùy chọn `n`.
```sh
tcpdump -n -i eth0
```
![Alt text](http://i.imgur.com/Ui5MyFZ.png)

Phần 1: Random Kernel Module
	- cd Random (chuyển directory đến folder chứa tập tin hello.c và Makefile)
	- make (Biên dịch driver tạo file hello.ko)
	- sudo insmod hello.ko (Nạp driver vào nhân hệ thống)
	- lsmod | grep hello (Xem thông tin số hiệu macro và module đã nạp)
	- dmesg (Xem thông tin driver)
	- head -cXX /dev/randomDevice | hexdump 
	- dd if=/dev/merandom bs=16 count=1 2>/dev/randomDevice| hexdump -C 
	(Đọc 16 bytes từ randomDevice và xuát ra dưới dạng hex)
	- sudo rmmod hello.ko (Gỡ cài đặt)


Phần 2: Hook syscall openat và syscall write
	- cd Hook (chuyển directory đến folder chứa tập tin hook.c và Makefile)
	- make
	- ls Hook (kiểm tra xem file hook.ko đã được tạo thành công hay chưa)
	- sudo insmod hook.ko (insert module)
	- dmesg -T (kiểm tra kết quả)
	- sudo rmmod hook (remove module)
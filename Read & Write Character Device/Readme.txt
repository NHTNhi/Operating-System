Device Driver
	- chuyển directory đến folder chứa tập tin driver.c và Makefile
	- make (Biên dịch driver tạo file driver.ko)
	- sudo insmod driver.ko (Nạp driver vào nhân hệ thống)
	- dmesg (Xem thông tin driver)
	- sudo -i và chạy lệnh
		+ echo -n "something" > /dev/mylog (write vào device)
		+ cat /dev/mylog (read device)
	- sudo rmmod driver.ko (Gỡ cài đặt)

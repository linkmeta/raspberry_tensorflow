1. raspi 配置命令
   raspi-config
   
2.查询温度
  vcgencmd measure_temp
  
3.工具
  vcgencmd commands
  
4.关机
  sudo shutdown -h now
  sudo halt
  sudo poweroff
  
5.查看内存情况
free -k

6.查看磁盘情况
df -h

7.打印该板子接口图
pinout

8.stream播放
./mjpg_streamer -i "./input_uvc.so -n -f 30 -r 1280x720" -o "./output_http.so -w ./www"
客户端：http://192.168.137.137:8080/?action=stream

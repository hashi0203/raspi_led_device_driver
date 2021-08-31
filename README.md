# raspi_led_device_driver

```bash
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo a > /dev/myled0
$ tail /var/log/syslog
...
Aug 31 03:47:37 ubuntu kernel: [1542589.641462] /home/ubuntu/raspi_led_device_driver/myled.c is loaded. major:499
Aug 31 03:49:32 ubuntu kernel: [1542704.807419] led_write is called
Aug 31 03:49:32 ubuntu kernel: [1542704.807435] led_write is called
```

```bash
$ sudo rmmod myled
```
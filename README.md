# raspi_led_device_driver

```bash
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ echo abc > /dev/myled0
$ tail /var/log/syslog
...
Aug 31 03:56:11 ubuntu kernel: [1543104.443591] /home/ubuntu/raspi_led_device_driver/myled.c is loaded. major:499
Aug 31 03:56:22 ubuntu kernel: [1543114.962910] receive a
Aug 31 03:56:22 ubuntu kernel: [1543114.962928] receive b
Aug 31 03:56:22 ubuntu kernel: [1543114.962940] receive c
Aug 31 03:56:22 ubuntu kernel: [1543114.962951] receive
Aug 31 03:56:22 ubuntu kernel: [1543114.962951]
```

```bash
$ sudo rmmod myled
```
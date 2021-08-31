# raspi_led_device_driver

```bash
$ make
$ sudo insmod myled.ko
```

```bash
$ tail /var/log/syslog
...
Aug 31 03:29:46 ubuntu kernel: [1541519.384880] /home/ubuntu/raspi_led_device_driver/myled.c is loaded. major:499
```

```bash
$ sudo mknod /dev/myled0 c 499 0
$ sudo chmod 666 /dev/myled0
$ echo a > /dev/myled0
$ tail /var/log/syslog
...
Aug 31 03:36:28 ubuntu kernel: [1541921.302421] led_write is called
Aug 31 03:36:28 ubuntu kernel: [1541921.302437] led_write is called
```

```bash
$ sudo rm /dev/myled0
$ sudo rmmod myled
```
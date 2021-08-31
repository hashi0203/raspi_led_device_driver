# raspi_led_device_driver

## 1. インストール

```bash
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
$ tail /var/log/syslog # ログを確認
...
Aug 31 04:05:47 ubuntu kernel: [1543679.899225] /home/ubuntu/raspi_led_device_driver/myled.c is loaded. major:499
```

## 2. LED 操作

```bash
$ echo 1 > /dev/myled0 # LED 点灯
$ echo 0 > /dev/myled0 # LED 消灯
```

## 3. アンインストール

```bash
$ sudo rmmod myled
$ tail /var/log/syslog # ログを確認
...
Aug 31 04:08:58 ubuntu kernel: [1543871.195933] /home/ubuntu/raspi_led_device_driver/myled.c is unloaded. major:499
```
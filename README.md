# Static-Routing

# How to configure Static Routing.

![image](https://github.com/user-attachments/assets/dca93d82-f7de-4f11-b4b6-9e510bcafb88)

 
## First configure PC1 ip address 192.168.10.2 255.255.255.0 and gateway 192.168.10.1

## Second configure Router1 

Conf t

Interface g0/0/1

Ip address 192.168.10.1 255.255.255.0

Description connected switch1

No shut

Int g0/0/0

Ip address 172.16.10.1 255.255.255.0

Description connected R2

No shut

## Do the same configuration with other side using network 192.168.20.0 255.255.255.0 and 172.16.20.0 255.255.255.255.0.

## Now you can configure static routing on Router2


Enable

Conf t

Ip route 192.168.20.0 255.255.255.255.0 172.16.20.1

Ip route 192.168.10.0 255.255.255.0 172.168.10.1

## Use command show ip route to see routing table

 ![image](https://github.com/user-attachments/assets/29bf20c1-b2d4-4052-ac8f-be5ba8c710bb)



## Ping PC1 to PC2 to test static routing protocol is working and now it is working

 .
![image](https://github.com/user-attachments/assets/7eaa0124-9990-4156-93dc-d638fc66e097)


![image](https://github.com/user-attachments/assets/a706d69e-bd12-4553-99a6-ff8526de6aae)


 

# Steps

## 1
`/interface bridge port remove [find interface =ether9]`

`/interface bridge port add bridge=bridge11 interface=ether9`

`/ip address add address=172.16.1.11/24 interface=ether1`

`/ip address add address=172.16.11.254/24 interface=ether2`

## 2
tux13:
`route add default gw 172.16.10.254`: 

![alt text](images/part2_exp4/2.jpeg)

tux14 and tux12:
`route add default gw 172.16.11.254`:

- RC -> `/ip route add dst-address=172.16.10.0/24 gateway=172.16.11.253`

- tux12 -> `route add -net 172.16.10.0/24 gw 172.16.11.253`

## 3

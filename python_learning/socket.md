![](/note_picture/spcket.png)

|socket类型|描述|
|--|--|
|socket.AF_UNIX|只能够用于单一的unix系统进程键通信|
|socket.AF_INET|IPv4|
|socket.AF_INET6|IPv6|
|socket.SOCK_STREAM|TCP|
|socket.DGRAM|UDP|
|socket.SOCK_RAW|原始套接字，普通的套接字无法处理ICMP、IGMP等网络报文，而SOCK_RAW可以；其次，SOCK_RAW也可以处理特殊的IPv4报文；此外，利用原始套接字，可以通过IP_HDRINCL套接字选项由用户构造IP头。|
|socket.SOCK_SEQPACKET|可靠的连续数据包服务|
|socket.SOCK_RDM|可靠的不连续数据包服务|
|socket.SOCK_PACKET|原始套接字，支持带有协议标识的数据包|

- 建立TCP连接 
    ```python
    s = socket(AF_INET, SOCK_STREAM)

    with socket.socket(AF_INET, SOCK_STREAM) as s
    # 不用with,不会自动关闭
    ```
## Net面试资料

**OSI七层模型**：物理层Ethernet、数据链路层ARP协议、网络层IP、传输层TCP/UDP、会话层RPC、表示层、应用层。

**传输层多路复用和分用**：将运输层报文段中的数据交付到正确的套接字的工作称为多路分解(demultiplexing),在源主机当中从不同的套接字中收集数据块，并为每一个数据块封装上首部信息(用于分解)从而生成报文段，然后将此报文段传递到网络层。所有的这些工作称为多路复用(multiplexing)。https://www.cnblogs.com/hithongming/p/9379397.html

**传输层和网络层的区别**：网络层负责ip数据报的产生以及ip数据包在逻辑网络上的路由转发，寻址是主机级别的。传输层提供端到端通信服务层次,提供可靠及非可靠连接，寻址是进程级的。网络层负责分组、路由和转发；传输层负责端口寻址、差错控制、拥塞控制等。https://blog.csdn.net/jinzhao1993/article/details/53354086

**UDP协议的特点**：无连接、面向报文、单播多播广播、头部开销小、无差错恢复拥塞控制、到达目的地是无序的、不可靠、但是速度快。https://cloud.tencent.com/developer/article/1405940 https://jaminzhang.github.io/network/The-Difference-Between-TCP-And-UDP-Protocol/

**UDP协议格式**：16位源端口、16位目的端口、16位报文长度、16位校验和，总共8字节的首部，外加数据。

**TCP协议的特点**：面向连接、面向字节流、只能点对点、头部长20个字节、可以进行差错恢复和拥塞控制、到达目的后会对乱序的包重排序、可靠交付、比较慢。

**TCP协议格式**：16位源端口、16位目的端口、32位序列号、32位确认序号、数据偏移|保留|六个状态位、16位窗口大小、16位校验和、16位紧急指针、32位选项和填充

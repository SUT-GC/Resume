# CPU缓存相关的知识

现在一般的CPU都是三级缓存，老得CPU可能是二级，三级缓存的话 L1和L2是跟着Core走的，也就是每个Core都有一套，L3是Cpu共享缓存，接下来就是RAM了。     

L1的速度是RAM的30倍所有     

L1的缓存一般有两部分，指令和数据，如果L1是64K的话，指令和数据各占32K     

三级缓存的目的就是为了减少对内存的读取，换句话说就是为了尽可能的弥补缓存和内存的速度差    

缓存Miss的话，就会涉及到读取内存数据，那么肯定不是一个一个的读，是一块一块的读，这个块就是Cache Line，一般CacheLine是64B, 那么32K/64B就是512个CacheLine        

保证缓存和内存的一致性，一般是用 Write Back (Write Behind Cache)      

一个数据在Core1的缓存上更新了， Core2就应该也读持有新的数据，则就需要缓存一致性的处理，解决缓存一致性一般有两种思路：      

* Directory 通过集中控制器来进行主要的控制和所有core的缓存变更     
* Snoopy 通过消息总线的方式，一个Core的缓存变更的时候，消息通知其他Core进行缓存状态的修改     

MESI 协议：缓存有4中状态，独占，共享，已修改，已无效    
MOESI协议：一个Core可以主动改另一个Core的缓存，那么就要增加一个 宿主状态     
MFESI协议：类似MOESI协议，但新增的状态不是 宿主态，而是 发送态，AMD是MOESI协议，Intel是MFESI协议     


# 参考文档    

* [https://coolshell.cn/articles/20793.html](https://coolshell.cn/articles/20793.html)

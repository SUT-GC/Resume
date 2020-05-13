# JAVA Class loader相关的知识

## Class Loader 用来做什么

用来将class文件加载成内存对象，文件可以来自磁盘文件，网络文件，而字节码的本质就是byte数组      

也因此，可以对class文件进行字节码加密，并且用定制的class loader 来加载加密后的字节码     

## 延迟加载

Class Loader 加载类并不是一次性的全部加载进来，只有用到这个类的时候，发现不认识这个类，才回去尝试加载     


## 双亲委派


Class Loader 内置有几个基础的      

* BootstrapClassLoader     
* ExtensionClassLoader     
* AppClassLoader     
* URLClassLoader      

BootstrapClassLoader是负责加载JVM运行时候的核心类库，这些类位于 JAVA HOME 下的rt.jar, 加载的类都是 java. 开头的，比如java.util, java.io, java.lang     

ExtensionClassLoader是负责加载java的扩展库，在JAVA HOME 下的ext目录下的jar包      

AppClassLoader 加载业务类，放在class path 下的jar包      

URLClassLoader 可以用来加载远程的类库，当然远程可以是网络上的，也可以是本地的，ExtensionClassLoader 和 AppClassLoader 就是URLClassLoader 的子类    

双亲委派就是JVM遇到一个不认识的类时候，先让BootstrapClassLoader加载，加载不到再让ExtensionClassLoader 加载，再让 AppClassLoader 加载      

tomcat的加载顺序相反     



## 自定义ClassLoad

* loadClass     
* findClass     
* defineClass     

loadClass里面。先让父类找，找不到调用findClass，findClass找到之后defineClass来拼装对象      

## ClassLoader 的隔离机制

每个ClassLoader加载的类是隔离的，就算是加载同一个类，也是不同的，但由于双亲委派，所以双亲加载的类会被孩子共享使用     

## 参考资料

* [https://juejin.im/post/5c04892351882516e70dcc9b](https://juejin.im/post/5c04892351882516e70dcc9b)

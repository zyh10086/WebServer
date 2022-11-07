# WebServer
22/11/7 update
解决了get请求文件夹时发生的段错误。

22/11/6 update
解决了无法在http报文数据段中写入较大文件的问题（根据每次writev写入数据量，对iovec结构体m_iv里的地址和长度进行修改），对content_type进行了判断，可以传输.css、.js等文件。



C++-牛客-Linux高并发服务器开发项目
locker.h主要对互斥锁、条件变量和信号量进行了封装。
threadpool.h实现了一个半同步/半反应线程池，由locker类互斥锁保证每个请求独占式的访问，sem类信号量实现多线程的同步。
http_conn.h、http_conn.cpp中实现了对http报文的读、写、解析。
main.cpp函数主要是使用epoll实现io多路复用,使用socket实现网络通信。


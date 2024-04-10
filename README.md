# Network-Security

1. 5大Web应用安全威胁
      1. 注入漏洞：攻击者在 应用程序接收用户输入的地方 注入自己精心构造的攻击代码，以达到执行任意操作、篡改数据或者获取敏感信息的目的。
         a. SQL 注入:           措施：对输⼊的特殊字符进⾏ Escape 转义处理、 对客户端输⼊进⾏控制，不允许输⼊ SQL 注⼊相关的特殊字符
         b. 命令注入:  web应用程序有时需要调用一些系统命令的函数，如system()，exec()等等，当用户能够控制这些函数中的参数时，就可以将恶意参系统命令拼接到正常命令中
         c. OS 注入：利用操作系统的漏洞，向服务器输入不受信任的数据，以利用操作系统上的缺陷来执行可疑操作。
         d. XML 注入：利用 XML 编辑器中的漏洞创建恶意 XML 代码的攻击
         
      2. 身份验证:  攻击者可以利用身份验证漏洞来模拟应用程序的合法用户。他们可能会使用：密码暴力破解、凭证填充、会话劫持、以及会话ID URL重写等方法，
         a. 凭证填充: 从一个
         b. 会话劫持：又称cookie劫持，攻击者接管合法用户的计算机会话以获取其会话ID，然后在任意数量的网络服务上充当该用户
                     可由XSS攻击实现（反射型：用户在登录的时候使用了攻击者的URL、存储型：攻击者事先将脚本存储到服务器端数据库中，只要用户浏览就被攻击、DOM型）    措施：对前端获取的数据进行转义处理。

      4. 敏感数据泄漏

      CSRF跨站请求伪造：利用伪造的HTTP请求登录上存在漏洞的Web应用程序     措施：验证referer、验证token
      SSRF服务器端请求伪造：攻击目标是从外网无法访问的内部系统
      XML外部实体注入：
      Webshell：利用文件上传漏洞，往目标网站中上传一句话木马

3. Web 访问过程分析

  ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/e291290f-35df-4c87-9bd8-52884d41f3fa)

  Web访问过程：
  ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/88341ecd-da54-4c5c-ae38-e12717272c19)

  一次Web访问过程分析：DNS域名解析、TCP连接、HTTP请求、web服务器处理请求并返回HTTP响应、如果有静态资源向CDN发起另外的请求、关闭TCP连接和页面渲染。
  
  
  CDN：内容分发网络，将内容缓存在终端用户附近

  TCP 和 UDP区别：
    连接方式：TCP是面向连接的，UDP是无连接的。
    数据传输方式：TCP是字节流，而UDP是数据报。
    可靠性：TCP提供可靠的传输，UDP不保证传输的可靠性。
    应用场景：TCP适用于稳定、可靠传输场景，UDP适用于实时性要求高或容忍数据丢失的场景。

  TCP 报文首部包括源端口号、目的端口号、序号字段、确认号字段、ACK、SYN
  
  TCP三次握手：
  ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/c2ca4ed1-1389-46dd-8770-37551fb3fc48)

  TCP四次挥手：
  ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/97843d61-7bdc-4c9d-84c7-1592d6dec78c)


3. 网络分层：

   ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/f0d9b97e-9e8b-456d-a3dc-243db2441466)

4. 网络分层和协议：

   ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/ef806791-032b-4084-9faf-f9c657703f91)

5.HTML5

   ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/767bde26-7b40-406b-8f0e-6965d6474ee0)

6.HTTP和HTTPS：

   ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/bb222d3d-c966-4ea1-b22e-f9ac31b64a71)


7. Linux Kali常用命令：
   
   ifconfig 命令用于获取网络接口设置与网络状态等信息
   who 用于查看当前登入主机的用户终端信息
   pwd 显示用户当前所处的工作目录
   ls 命令可以用来查看当前工作路径下所有非隐藏的文件
   cat 命令用于查看纯文本文件
   sudo 以系统管理者的身份执行指令

   
nmap是一款非常强大的主机发现和端口扫描工具
-sT 使用TCP进行扫描
-sU  UDP扫描
-p    扫描指定端口



8. 动态服务器页面：
   
  ![图片](https://github.com/Jonas9172/Network-Security/assets/105164575/c3dd7ce4-c93e-4b83-9f30-e57a5fd0be9e)







   


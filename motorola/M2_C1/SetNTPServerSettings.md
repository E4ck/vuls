# Motorola SetStaticRouteSettings CMD Injection

Product:
* Motorola C1 (Refer: http://www.soplar.cn/moluyou.html)
* Motorola M2 (Refer: http://www.soplar.cn/moluyou.html)


Version: The latest firmware:

* C1: 1.01(Download Link: http://www.soplar.cn/download/C1.zip)
* M2: 1.07(Download Link: http://www.soplar.cn/download/M2.zip)

![](imgs/2019-02-19-11-44-07.png)

Vulnerability Type: Command Injection

Institution: 360 ESG / Legendsec Information Technology(Beijing)Inc..

## Vulnerability Description

A command Injection vulnerability allows attackers to execute arbitrary OS commands via a crafted /HNAP1 POST request. This occurs when any HNAP API function triggers a call to the `system` function with untrusted input from the request body for the `SetNTPServerSettings` API function, as demonstrated by shell metacharacters in the `system_time_timezone` field


## POC

![](imgs/2019-02-19-15-03-31.png)


![](imgs/2019-02-19-15-04-07.png)
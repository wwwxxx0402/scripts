# 学会使用查找功能！Ctrl+F
# DD网络重装脚本：系统默认为debian12
## moeclub大佬的脚本

```sh
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/MoeClub/Note/master/InstallNET.sh') -d 12 -v 64 -p 密码 -port 端口 -a -firmware
```
## leitbogioro大佬的脚本（推荐）
```sh
wget --no-check-certificate -qO InstallNET.sh 'https://raw.githubusercontent.com/leitbogioro/Tools/master/Linux_reinstall/InstallNET.sh' && chmod a+x InstallNET.sh && bash InstallNET.sh -debian 12 -pwd '密码'
```
## beta.gs大佬的脚本
```sh
wget --no-check-certificate -O NewReinstall.sh https://raw.githubusercontent.com/fcurrk/reinstall/master/NewReinstall.sh && chmod a+x NewReinstall.sh && bash NewReinstall.sh
```

# 服务器综合测试脚本（融合怪）（推荐）GitHub开源地址
```sh
 curl -L https://gitlab.com/spiritysdx/za/-/raw/main/ecs.sh -o ecs.sh && chmod +x ecs.sh && bash ecs.sh
```
# 性能测试脚本
## YABS（推荐）GitHub开源地址
```sh
wget -qO- yabs.sh | bash
```
## 流量稀缺的服务器（不测试iperf网络）
```sh
curl -sL yabs.sh | bash -s -- -i
```
## 我更喜欢geekbench5（不测试geekbench6）
```sh
curl -sL yabs.sh | bash -s -- -5
```
## 我喜欢geekbench5，但服务器流量稀缺（不测试geekbench6、不测试iperf网络）
```sh
curl -sL yabs.sh | bash -s -- -5 -i
```
## Geekbench 5 专测脚本 GitHub开源地址 论坛大佬@Google 开发
```sh
bash <(curl -sL gb5.top)
```
## LemonBench GitHub开源地址
```sh
wget -qO- https://raw.githubusercontent.com/LemonBench/LemonBench/main/LemonBench.sh | bash -s -- --fast
```
## UnixBench.sh
```sh
wget --no-check-certificate https://github.com/teddysun/across/raw/master/unixbench.sh
chmod +x unixbench.sh
./unixbench.sh
```
# 网络测试脚本
## hyperspeed 三网测速（推荐）（未开源）
```sh
bash <(curl -Lso- https://bench.im/hyperspeed)
```
## AutoTrace 三网回程线路显示（推荐）
```sh
wget -N --no-check-certificate https://raw.githubusercontent.com/Chennhaoo/Shell_Bash/master/AutoTrace.sh && chmod +x AutoTrace.sh && bash AutoTrace.sh
```
## backtrace 三网回程线路直接显示（小白用这个）
```sh
curl https://raw.githubusercontent.com/zhanghanyun/backtrace/main/install.sh -sSf | sh
```
## Bench 网络带宽及硬盘读写速率（国外部分+国内部分节点）
```sh
wget -qO- bench.sh | bash
```
## SuperBench.sh 网络带宽及硬盘读写速率（国内三网+speedtest+fast）
```sh
wget -qO- --no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```
## 网络 专测 论坛大佬@Google开发
```sh
bash <(curl -sL https://raw.githubusercontent.com/i-abc/Speedtest/main/speedtest.sh)
```
# 超售测试脚本
## 一键检测超售 LOC帖
```sh
wget --no-check-certificate -O memoryCheck.sh https://raw.githubusercontent.com/uselibrary/memoryCheck/main/memoryCheck.sh && chmod +x memoryCheck.sh && bash memoryCheck.sh
```
## 移除virtio_balloon模块
```sh
rmmod virtio_balloon
```
## 内存填充测试
```sh
apt-get update
apt-get install wget build-essential -y
wget https://raw.githubusercontent.com/FunctionClub/Memtester/master/memtester.cpp
gcc -l stdc++ memtester.cpp
./a.out
```
# 流媒体测试脚本
## RegionRestrictionCheck（推荐）
```sh
bash <(curl -L -s check.unlock.media)
```
## 流媒体解锁改（加入了原生/DNS解锁检测）
```sh
bash <(curl -L -s media.ispvps.com)
```
## openai解锁检测
```sh
bash <(curl -Ls https://github.com/ludashi2020/OpenAI-Checker/raw/main/openai.sh)
```
# BBR脚本
## 一键开启BBR（适用于较新的Debian、Ubuntu）
```sh
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
sysctl -p
sysctl net.ipv4.tcp_available_congestion_control
lsmod | grep bbr
```
## Linux-NetSpeed（锐速/bbrplus/bbr魔改版）
```sh
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
chmod +x tcp.sh
./tcp.sh
```
## ylx大佬的锐速/BBRPLUS/BBR2
```sh
wget -O tcpx.sh "https://github.com/ylx2016/Linux-NetSpeed/raw/master/tcpx.sh" && chmod +x tcpx.sh && ./tcpx.sh
```
# moerats大佬的添加swap脚本
```sh
wget https://www.moerats.com/usr/shell/swap.sh && bash swap.sh
```
# spiritlhl大佬的zram内存压缩脚本
```sh
curl -L https://raw.githubusercontent.com/spiritLHLS/addzram/main/addzram.sh -o addzram.sh && chmod +x addzram.sh && bash addzram.sh
```
# cloudflare warp脚本 添加IPv4/IPv6网络
```sh
wget -N https://gitlab.com/fscarmen/warp/-/raw/main/menu.sh && bash menu.sh
```
# fail2ban服务器ssh防爆破
```sh
wget https://raw.githubusercontent.com/FunctionClub/Fail2ban/master/fail2ban.sh && bash fail2ban.sh 2>&1 | tee fail2ban.log
```
# 独立服务器硬盘时间
```sh
wget -q https://github.com/Aniverse/A/raw/i/a && bash a
```
# 常用软件脚本
## Docker
```sh
curl -sSL https://get.docker.com/ | sh
```
## Nezha探针 官网
```sh
curl -L https://gitee.com/naibahq/nezha/raw/master/script/install.sh -o nezha.sh && chmod +x nezha.sh && sudo ./nezha.sh
```
## Alist V3一键安装 官网
```sh
curl -fsSL "https://alist.nn.ci/v3.sh" | bash -s install
```
## Aria2一键安装脚本
```sh
wget -N git.io/aria2.sh && chmod +x aria2.sh && bash aria2.sh
```
## XUI
```sh
bash <(curl -Ls https://raw.githubusercontent.com/FranzKafkaYu/x-ui/master/install.sh)
```
## Xray
```
bash -c "$(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh)" @ install
```
## qbittorrent 4.3.9

[安装教程](https://hostloc.com/thread-1024684-1-1.html)
# 其他

[VPS剩余价值计算器 @nanyi](https://www.nodeseek.com/space/7658#/discussions)

[全国 34 省份 TCPING v4 IP](https://www.nodeseek.com/post-68572-1)

[北上广四网TCPing可用地址](https://www.nodeseek.com/post-56429-1)
## 宝塔一键挂载硬盘脚本
```sh
wget -O auto_disk.sh http://download.bt.cn/tools/auto_disk.sh && bash auto_disk.sh
```
## acme生成免费证书
```sh
curl https://get.acme.sh | sh
```
## 剑皇刷流量脚本
```sh
wget https://cdn.jsdelivr.net/gh/maintell/webBenchmark@releases/download/0.6/webBenchmark_linux_x64
chmod +x webBenchmark_linux_x64
./webBenchmark_linux_x64 -c 64 -s http://链接.jpg
```
## 测试 25 端口是否开放
```sh
telnet smtp.aol.com 25
```
## 测试 IPv4 优先还是 IPv6 优先
```sh
curl ip.p3terx.com
```
```sh
curl ip.sb
```
## 一键删除平台监控(阿里云、腾讯云、华为云、UCLOUD、甲骨文云、京东云)
```sh
curl -L https://raw.githubusercontent.com/spiritLHLS/one-click-installation-script/main/install_scripts/dlm.sh -o dlm.sh && chmod +x dlm.sh && bash dlm.sh
```

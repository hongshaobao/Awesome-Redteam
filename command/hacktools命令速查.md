# 端口扫描

```
# nmap
nmap -sS -Pn -n --open --min-hostgroup 4 --min-parallelism 1024 --host-timeout 30 -T4 -v -p 1-65535 -iL ip.txt -oX output.xml
```

```
# fscan
fscan -hf hosts.txt --nopoc -t 100
```

# AlliN

```# Arjun
# 按域名爬取
python AlliN.py --host $host -m subscan --project $project --timeout 6

# 按文件爬取
python AlliN.py -f domain.txt
```

# Arjun

```SHELL
# Scan a single URL
arjun -u https://api.example.com/endpoint

# Specify HTTP method
arjun -u https://api.example.com/endpoint -m POST

# Import targets
arjun -i targets.txt

# Export result
arjun -u https://api.example.com/endpoint -oJ result.json
-----------------
-oJ result.json
-oT result.txt
-oB 127.0.0.1:8080
```

# Dirsearch

```
# 参数
-u 目标
-e 文件扩展名
-x 排除状态码结果
-w 指定字段
-r 递归扫描
-R 设置递归级别
-t 设置线程数（50-100）
-c cookie
```

```python
# 自定义字典
python3 dirsearch.py -e php,html,js -u https://target -w /path/to/wordlist
```

# Dirmap

```python
# 单目标
python dirmap.py -i https://target.com -lcf
python dirmap.py -i 192.168.1.1 -lcf

# 子网
python dirmap.py -i 192.168.1.0/24 -lcf

# 网络范围
python dirmap.py -i 192.168.1.1-192.168.1.100 -lcf

# 文件读取
python dirmap.py -iF targets.txt -lcf
```

# EHole

```shell
# 系统指纹探测
# 本地识别
EHole -l url.txt   //URL地址需带上协议,每行一个

# FOFA识别
EHole -f 192.168.1.1/24  //支持单IP或IP段

# 结果输出
EHole -l url.txt -json export.json  //结果输出至export.json文件
```

# ENScan_GO

```SHELL
# 企业信息收集
ENScanPublic_amd64_linux -n 小米

# 备案信息获取
ENScanPublic_amd64_linux -n 小米  -field website
```

# ksubdomain

```shell
# 使用内置字典爆破
ksubdomain -d seebug.org

# 使用字典爆破域名
ksubdomain -d seebug.org -f subdomains.dict

# 字典里都是域名，可使用验证模式
ksubdomain -f dns.txt -verify
```

# OneForAll

```python
python oneforall.py --target example.com run
python oneforall.py --targets ./example.txt run
```

# SQLmap

```python
python sqlmap.py -u  "https://xxx.xxx" --dbs
```

# Xray

- https://github.com/chaitin/xray

```shell
# 网络扫描
.\xray_windows_386.exe webscan --listen 127.0.0.1:7777 --html-output xray.html

# 服务扫描
.\xray_windows_386.exe servicescan -t 127.0.0.1:7777

# 指定插件
xray webscan --plugins cmd-injection,sqldet --url http://example.com
xray webscan --plugins cmd-injection,sqldet --listen 127.0.0.1:7777
```

# 图片马制作

```
copy 1.jpg/b+1.php/a 2.jpg
```

# ppshuai_ExchangeDataCollection
上海期货交易所、大连期货交易所、郑州期货交易所、中国金融交易所国内四大交易所的龙虎榜数据采集统一

# Linux安装依赖
sudo yum install -y openssl-devel libcurl-devel jsoncpp-devel unzip

sudo yum install -y centos-release-scl

sudo yum install -y devtoolset-8-toolchain

sudo yum install -y python3

python3 -m pip install xlrd

```
# new create bash environment
#scl enable devtoolset-8 bash

# current bash environment
source /opt/rh/devtoolset-8/enable

source scl_source enable devtoolset-8

g++ -o main.out main.cpp -ljsoncpp -lssl -lcrypto -lcurl
```

# 运行方式
./ExchangeDataCollection "/home/pps/data/"

./ExchangeDataCollection 2019 11 13

./ExchangeDataCollection "/home/pps/data/"

# 部署
nohup ./ExchangeDataCollection "/home/pps/data/" > edc.log 2>&1 &
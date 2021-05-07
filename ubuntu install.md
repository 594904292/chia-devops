cd /media/sda
ls
mkdir tmp1
mkdir tmp2
mkdir tmp3
mkdir tmp4

wget https://github.com/hpool-dev/chia-plotter/releases/download/v0.11/chia-plotter-v0.11-x86_64-linux-gnu.zip
wget https://github.com/hpool-dev/chia-miner/releases/download/v1.1.1/HPool-Miner-chia-v1.1.1.zip
apt install unzip
apt install iotop

unzip chia-plotter-v0.11-x86_64-linux-gnu.zip -d chia-plotter-v0.11-x86_64-linux-gnu
unzip HPool-Miner-chia-v1.1.1.zip -d HPool-Miner-chia-v1.1.1
ls
cd chia-plotter-v0.11-x86_64-linux-gnu/
ls
cd chia-plotter/
ls
pwd
df -h
(./chia-plotter-linux-amd64 -action plotting -plotting-fpk 0x8ff08e4b18c676d11876f2e2ffd092dd28a1bb739de99ec67a2e3642d183c34ac445bf3c13cb0019c382c390b08c240e -plotting-ppk 0xaac5afce034d9fc17364cb25f94f939c1b1783ec21c7553b4dba5bc1390b1d4b782ae481491a33367034067a359b7509 -plotting-n 100 -d /media/sdb -t /media/sda > nohup1.out &)
(./chia-plotter-linux-amd64 -action plotting -plotting-fpk 0x8ff08e4b18c676d11876f2e2ffd092dd28a1bb739de99ec67a2e3642d183c34ac445bf3c13cb0019c382c390b08c240e -plotting-ppk 0xaac5afce034d9fc17364cb25f94f939c1b1783ec21c7553b4dba5bc1390b1d4b782ae481491a33367034067a359b7509 -plotting-n 100 -d /media/sdb -t /media/sda/tmp2 > nohup2.out &)
(./chia-plotter-linux-amd64 -action plotting -plotting-fpk 0x8ff08e4b18c676d11876f2e2ffd092dd28a1bb739de99ec67a2e3642d183c34ac445bf3c13cb0019c382c390b08c240e -plotting-ppk 0xaac5afce034d9fc17364cb25f94f939c1b1783ec21c7553b4dba5bc1390b1d4b782ae481491a33367034067a359b7509 -plotting-n 100 -d /media/sdb -t /media/sda/tmp3 > nohup3.out &)
(./chia-plotter-linux-amd64 -action plotting -plotting-fpk 0x8ff08e4b18c676d11876f2e2ffd092dd28a1bb739de99ec67a2e3642d183c34ac445bf3c13cb0019c382c390b08c240e -plotting-ppk 0xaac5afce034d9fc17364cb25f94f939c1b1783ec21c7553b4dba5bc1390b1d4b782ae481491a33367034067a359b7509 -plotting-n 100 -d /media/sdb -t /media/sda/tmp4 > nohup4.out &)
ls
ps -ef | grep chia
tail -f nohup1.out
tail -f nohup2.out
tail -f nohup3.out
tail -f nohup4.out
ls
top
iotop
ps -ef | grep chia
ls
cd ..
ls
cd
l
cd HPool-Miner-chia-v1.1.1/
cd linux/
vim config.yaml
'''config.yaml
token: ""
path:
- /media/sdb
minerName: "16018877188"
apiKey: 27fa48b4-342c-4d1b-9bc3-b72bd3e40608
cachePath: ""
deviceId: ""
extraParams: {}
log:
  lv: info
  path: ./log/
  name: miner.log
url:
  info: ""
  submit: ""
  line: ""
scanPath: true
scanMinute: 10
debug: ""
'''
(./hpool-miner-chia &)
ps -ef | grep chia

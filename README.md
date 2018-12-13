# packet_repeater
IEEE 802.15.4パケットをインターネット越しに送る用のプログラム

## Usage
リレーサーバー上で以下を実行
```
gcc relay_server.c watalib.h
 ./relay.out
```

上流側基地局では
```
gcc frontend_15.4_source.c watalib.h
sudo ./frontend_source.out /dev/ttyUSB0 [ip_addr] [port_num]
```
一応 `run_source_client.sh` を書き換えると簡単に書き換えできる．

下流側基地局では
```
gcc frontend_15.4.c watalib.h
sudo ./frontend.out /dev/ttyUSB0 [ip_addr] [port_num]
```
一応 `run_client.sh` を書き換えると簡単に書き換えできる．

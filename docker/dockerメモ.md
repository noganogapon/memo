# dockerコンテナからホストマシンのポートにアクセスする方法

デフォルトではdockerコンテナから、ホストマシンにネットワーク接続することはできない。

以下のようにルーティングを設定する必要がある

iptables -I INPUT 4 -i docker0 -j ACCEPT

http://stackoverflow.com/questions/31324981/how-to-access-host-port-from-docker-container

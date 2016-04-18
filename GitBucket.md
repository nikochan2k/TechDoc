# UbuntuにGitBucketをインストール
## Javaのインストール
[UbuntuにJava 1.8をインストールする](./GitBucket.md)
## Jetty
### インストール
```
sudo apt-get install jetty8
```
### 設定
```
vi /etc/default/jetty8
```
* 起動可能にする
```
# change to 0 to allow Jetty to start
#NO_START=1
NO_START=0
```
* 外部からアクセスできるようにする
```
# Listen to connections from this network host
# Use 0.0.0.0 as host to accept all connections.
# Uncomment to restrict access to localhost
#JETTY_HOST=$(uname -n)
JETTY_HOST=0.0.0.0
```
* メモリを増やす
```
# Extra options to pass to the JVM
#JAVA_OPTIONS="-Xmx256m -Djava.awt.headless=true"
JAVA_OPTIONS="-Xmx1024m -Djava.awt.headless=true"
```
* JAVA_HOMEの設定
```
# Home of Java installation.
#JAVA_HOME=
JAVA_HOME=/usr/lib/jvm/java-8-oracle
```
* GITBUCKET_HOME環境変数を追加
```
GITBUCKET_HOME=/var/lib/jetty8
```

## GitBucket

### GitBucketのインストール
```
cd /usr/share/jetty8/webapps
sudo wget https://github.com/gitbucket/gitbucket/releases/download/3.13/gitbucket.war
sudo chown jetty:adm gitbucket.war
```

## Jettyの起動
```
sudo service jetty8 restart
```

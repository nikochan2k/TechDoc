# UbuntuにJava 1.8をインストールする

## 準備
### apt-add-repositoryを利用できるようにする
```
sudo apt-get install software-properties-common
```
### Javaのリポジトリを追加する
```
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
```
## Javaのインストール
### Java本体
```
sudo apt-get install oracle-java8-installer
```
### 環境変数
```
sudo apt-get install oracle-java8-set-default
```

## 参考
* [ubuntu 14.04 でのapt-add-repositoryのインストール](http://qiita.com/Hiroshi_Obata/items/8fa13972f7922ad3252f)
* [Ubuntu にOracle Java 8 (PPA)をインストールする](http://qiita.com/TsutomuNakamura/items/f12fdf0a8502e634584d)

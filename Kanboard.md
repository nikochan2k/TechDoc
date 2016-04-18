# Kanboard

## 関連モジュールのインストール
```
sudo apt-get install php5 php5-sqlite php5-mysql php5-pgsql php5-ldap php5-gd php5-json php5-mcrypt unzip
```
## Kanboardのインストール
```
cd /var/www/html
sudo wget http://kanboard.net/kanboard-latest.zip
sudo unzip kanboard-latest.zip
sudo chown -R www-data:www-data kanboard/data
sudo rm kanboard-latest.zip
```
## ログイン
adnim/adminでログイン
## 設定
* 右上部のアイコンからSettingsをクリック

### Application Settings
* Application URLを設定
* Languageを「日本語」に設定
* Timezoneを「Asia/Tokyo」に設定
* Date and time formatを「YYYY/MM/DD HH:mm」に設定

すべて設定したら「Save」をクリック
### 為替レート
* 基軸通貨「日本円」

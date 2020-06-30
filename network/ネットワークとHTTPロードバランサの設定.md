
# ネットワークとHTTPロードバランサーの設定
https://google.qwiklabs.com/focuses/12007?parent=catalog

## gcloud設定
 1. アクティブなアカウント名確認コマンド
 ```  gcloud auth list ```
 
 1. デフォルト設定プロジェクトID確認コマンド
 ```gcloud config list project```
 1. デフォルトのゾーン設定コマンド
  ```gcloud config set compute/zone us-central1-a```
 1. デフォルトのリージョン設定コマンド
  ```gcloud config set compute/region us-central1``` 
  
 ## 環境構築（webサーバーインスタンスを用意する）
 1. webサーバインスタンスで使用するnginxをセットアップするスクリプトの作成
 ```cat << EOF > startup.sh #! /bin/bash apt-get update apt-get install -y nginx service nginx start sed -i -- 's/nginx/Google Cloud Platform - '"\$HOSTNAME"'/' /var/www/html/index.nginx-debian.html EOF
 ```
 1. 
 
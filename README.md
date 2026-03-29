# AWS インフラ構築ポートフォリオ

## 概要
AWS上にWebサーバー環境を構築し、ALB + Auto Scaling構成で公開しました。

## 構成図
![構成図](architecture.png)

## 使用技術
- AWS（EC2, ALB, Auto Scaling, Route53）
- Linux（Ubuntu）
- Nginx
- SSH（踏み台サーバー）

## 構成
Internet → Route53 → ALB → EC2（Auto Scaling）→ Nginx

## 主な作業内容
- EC2構築・SSH接続
- Nginxインストール・Web公開
- ALB設定
- Auto Scaling構成
- 独自ドメイン設定
- HTTPS化
- ログ確認（access.log）
- 障害対応（Nginx停止 → ログ解析）

## 工夫した点
- Auto Scalingで可用性を確保
- ログを用いたトラブルシュートを実施
- 踏み台サーバー経由のSSH構成

## 動作確認
https://uforiasatosgear.jp

## 今後の改善
- CloudFront導入
- WAF強化
- CI/CD導入

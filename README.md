# なにこれ？

あなたのSlackワークスペース内のホットなチャンネルをおしらせします。

# 開発経緯

参加中のSlackコミュニティ内でアクティブなチャンネルがわからなかった。
アクティブなチャンネルを探すには1つ1つ中身を開いていく必要がある上、新しいチャンネルが日に日に増えていくため
簡単に可視化するツールが欲しかった。

# 使い方

このプロジェクトはGithub Actionsによりバッチ処理ができるようになっています。
forkを使用し、設定（Secretを使用）を行うだけで比較的簡単に使えます！

# 設定方法

Slack Appの作成と、トークンの取得が必要です。

## 1. Slack App を作成します。
- Your Apps > Create New App 
	- App Name : 任意の名称 (slack-hot-channel-bot 等) を入力します。
	- Development Slack Workspace : 通知したいワークスペースを選択します。

## 2. トークン を取得します。
- Basic Information > App Credentials > Verification Token の値をメモします。

## 3. Incoming Webhook のURLを取得します。
- Incoming Webhook > Activate Incoming Webhooks > On にします。
- Incoming Webhook > Webhook URL の値をメモします。

## 4. Github Actions を設定します。
- Github > Settings > Secrets より、下記設定を行います。
	- SLACK_API_TOKEN : 2. で取得したトークンを設定します。
	- SLACK_WEBHOOK_ENDPOINT : 3. で取得したURLを設定します。
	- TITLE : 任意のタイトルを設定します。

- /.github/workflows/batch.yml を元に Actions を設定します。

# 利用者

-  弱弱エンジニア会

利用者に追加してほしいコミュニティがあればPRください！

# ライセンス

MIT License

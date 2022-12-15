# 概要

Nginxの設定の動作確認用環境

# 構成

nginx1（リバースプロキシ）→ nginx2（コンテンツ）

# 実行

```
# 実行開始
> docker compose up -d

# ログの確認
> docker compose logs -f
```

設定ファイル更新後は

```
> docker compose restart
```
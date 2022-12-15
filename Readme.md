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

## ブラウザ確認

rewriteの設定がない場合は、以下のような動作になる

- `http://localhost/sub/index.html`で`nginx2/www/sub/index.html`に遷移する
- `http://localhost/index.html`で`nginx2/www/index.html`に遷移する


# 環境破棄/停止

```
# 破棄
docker compose down

# 停止
docker compose stop
```
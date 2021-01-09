# 静的ファイルを配信しよう！ | django #3

第3回はdjangoの静的ファイル（画像、音声、CSSデータなど）の配信の仕方を覚えるのが目標です。

## 完成版プロジェクト＆テキスト

https://github.com/shun-rec/django-website-03

## 前回のプロジェクト

https://github.com/shun-rec/django-website2

## コピペ用コマンド

### Whitenoiseのインストール

インストール

```sh
pip install whitenoise
```

全体設定の最後に以下を追記

```py
STATIC_URL = '/assets/'
STATIC_ROOT = os.path.join(BASE_DIR, 'staticfiles')

STATICFILES_STORAGE = 'whitenoise.storage.CompressedManifestStaticFilesStorage'
```

### 静的ファイルを一箇所に集める

```py
python manage.py collectstatic
```

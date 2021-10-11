## vboxsf
vbboxsfでエラーが発生した場合は
vagrant plugin install vagrant-vbguest
を実行する

## 手動実行箇所

php.ini の変更(root実行)
```text
date.timezone = "Asia/Tokyo"
mbstring.language = Japanese
mbstring.internal_encoding = UTF-8
mbstring.http_input = pass
mbstring.http_output = pass
mbstring.encoding_translation = Off
mbstring.detect_order = auto
mbstring.substitute_character = none;
mbstring.strict_detection = Off
```

## Laravelインストール

```text
composer create-project --prefer-dist laravel/laravel data "6.*"
```

## VueCliインストール

```text
npm install -g @vue/cli
```

## 備考
初回vagrant upではshardフォルダの権限がrootになっています。  
一度vagrant halt してから　vagrant upし直してくださいぎ。  


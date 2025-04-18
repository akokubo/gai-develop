# Homebrewのインストール

## ターミナルの起動

[アプリケーション]→［ユーティリティ］→[ターミナル]

## Homebrewのインストール
ターミナルで
```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
パスワードを聞かれたら打つ

## Homebrewの設定
ターミナルで

```sh
echo >> ~/.zprofile
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

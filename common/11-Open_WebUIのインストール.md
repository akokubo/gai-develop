# Open WebUIのインストール

## 仮想環境に入っていなければ入る

### Windowsの場合
Ubuntuで
```sh
python3 -m venv ~/venv-llm
```

### macOSの場合
ターミナルで
```sh
conda activate conda-llm
```
## Open WebUIのインストール
```sh
python3 -m pip install open-webui
```

## Open WebUIの起動
```sh
open-webui serve
```

## Open WebUIへのアクセス

ブラウザで以下にアクセス
```
http://localhost:8080/
```

初回は、[Get Started]の上の右矢印をクリックする。
そして、名前(表示名)、メールアドレス、(ログイン)パスワードを登録する。

## Open WebUIの終了
終了するには<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">Ctrl</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">C</kbd>

## Open WebUIのアップデート
```sh
python3 -m pip install open-webui -U
```

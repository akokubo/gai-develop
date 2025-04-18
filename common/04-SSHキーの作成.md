# SSHキーの作成

## SSHとは
SSH(Secure Shell)では、通信を暗号化して、ネットワーク越しにアクセスできる。

暗号化には、公開鍵暗号と共通鍵暗号を併用している。
最初に安全だが処理が重い公開鍵暗号で共通鍵を交換し、その後の通信は高速な共通鍵暗号が用いられる。

公開鍵暗号には公開鍵と秘密鍵がある。
それぞれコンピュータに保存される。

秘密鍵は漏れるとまずいので、コンピュータに保存するときに更に共通鍵暗号で、暗号化する仕様になっている。
秘密鍵の暗号化に使うパスワードのことを「パスフレーズ」と呼ぶ。

秘密鍵を使うときには、秘密鍵にかけられた暗号を復号化する必要があるので、パスフレーズは毎回入力を求められる。

これは煩雑なため、空のパスフレーズを設定することもできる。
空のパスフレーズを設定した場合、パスフレーズの入力は求められなくなり、楽になる。
ただし、その場合、秘密鍵を保存したファイルには生の秘密鍵が入っているので、漏洩すると大変まずいことになる。

## SSHキーの作成コマンドの実行
Windowsでは「Ubuntu」、macOSでは「ターミナル」を起動し、以下のように打つ。

```sh
ssh-keygen -t ed25519 -C メールアドレス
```

## SSHキーの保存ファイル名の指定

SSHキーを保存するファイル名を聞かれる

```sh
Enter file in which to save the key (ファイル名):
```

そのままでいい場合は、単に <kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">Enter</kbd>。

ここで指定したファイルが既に存在していた場合、進めていくと以下のように「上書きするか」と聞かれる。

```sh
Overwrite (y/n)
```

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">n</kbd>だと上書きしないので、そこで一旦終了する。
その場合は、再度実行し、別のファイル名を付ける。

## パスフレーズの指定

パスフレーズを入力するように2回言われるので、2回同じものを打つ。

```sh
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```

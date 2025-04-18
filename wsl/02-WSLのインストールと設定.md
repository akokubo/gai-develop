# WSLのインストールと設定

## 参考
* https://learn.microsoft.com/ja-jp/windows/wsl/install
* https://learn.microsoft.com/ja-jp/windows/wsl/basic-commands

## WSLの最新版をダウンロード

以下にアクセスして

https://github.com/microsoft/WSL/releases

Latest(最新バージョン)の .msi をCPUに合わせてダウンロード

このファイルの作成時点の最新版は2.4.13。

CPUは、Intelはx64、AMDはarm64。

## ダウンロードした .msi をインストール

ダウンロードした .msi をダブルクリックしてインストールする

## WSLをインストール

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;"><span class="Unicode">⊞</span> Win</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">S</kbd>
で検索を起動し、「powershell」を検索し、「Windows PowerShell」を右クリックし、「管理者として実行」をクリックする

Windows PowerShellで以下のように打って実行

```sh
wsl --install
```

インストールが終わったら、Windowsを再起動

## WSLをアップデート

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;"><span class="Unicode">⊞</span> Win</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">S</kbd>
で検索を起動し、「powershell」を検索し、「Windows PowerShell」を右クリックし、「管理者として実行」をクリックする

Windows PowerShellで以下のように打つ。

```sh
wsl --update
```

## Ubuntuのインストール

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;"><span class="Unicode">⊞</span> Win</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">S</kbd>
で検索を起動し、「powershell」を検索し、「Windows PowerShell」を右クリックし、「管理者として実行」をクリックする

2回目になるが、Windows PowerShellで以下のように打って実行

```sh
wsl --install
```

## Ubuntuのユーザー設定

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;"><span class="Unicode">⊞</span> Win</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">S</kbd>
で検索を起動し、「ubuntu」を検索し、「Ubuntu」をクリックする。

初回は、ユーザー名とパスワードを設定するように言われる。
このユーザー名とパスワードは、Windowsとは独立に設定できる(同じにしてもいい)。

まず「Create a default Unix user account:」に続けて表示されるのがデフォルトのユーザー名の提案である。
これはWindowsのユーザー名の先頭5文字程度になっている。
これを適宜修正する。
日本語は使えない。

次に「New password:」にUbuntuで使うパスワードを指定する。
なお、パスワードは打っても見えない。
これは以降も同様。

次に「Retype new password:」にもう一度パスワードを打つ。

## Ubuntuの更新

Ubuntuで以下のように打つ。

```sh
sudo apt update
sudo apt upgrade
```
なお、「sudo」を打つと、パスワードを聞かれるので打つ(見えない)。
以降も同様。

また、[Y/n]と聞かれたら <kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">y</kbd>

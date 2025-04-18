# Python venv仮想環境の作り方

## 1. WSLを起動

<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;"><span class="Unicode">⊞</span> Win</kbd>
+
<kbd class="keyboard-key nowrap" lang="en" style="border: 1px solid #aaa; border-radius: 2px; box-shadow: 1px 2px 2px #ddd; background-color: #f9f9f9; background-image: linear-gradient(top, #eee, #f9f9f9, #eee); padding: 1px 3px; font-family: inherit; font-size: 0.85em;">S</kbd>で検索を起動し、「ubuntu」を検索し、「Ubuntu」をクリックしてWSLを起動する

## 3. 「プロンプト」とは
「プロンプト」とは、コンピュータ関連では主に2つの意味がある。

一つは、文字を打ってコンピュータに指示をする、コマンド・ライン・インタフェース(CLI)で、現在入力が可能な状態であることを示す
「\>」「\$ 」「% 」などである。
「入力促進記号」とも言われる。

もう一つは、生成AIに対する文字での「指示」のことである。

## 4. 「プロンプト」の確認

「入力促進記号」の方のプロンプトを確認する。

プロンプトが「(仮想環境名) ユーザー名@コンピュータ名:~\$ 」のようになっていれば、既に仮想環境に入っている。

プロンプトが「ユーザー名@コンピュータ名:~\$ 」のようになっている場合は、仮想環境に入っていない。

## 5. 仮想環境がなければ作る

任意のディレクトリに作れるが、今回はいろいろな開発で共通に使うことを想定し、ホーム・ディレクトリに作る。

ホーム・ディレクトリに移動
```sh
cd
```

「venv-llm」という名前の仮想環境を作る。名前は他のものでもいい。

```sh
python3 -m venv venv-llm
```

## 6. 仮想環境に入る

```sh
source ~/venv-llm/bin/activate
```

## 7. プロンプトを確認

プロンプトが「(仮想環境名) ユーザー名@コンピュータ名:~\$ 」のようになれば、仮想環境に入った。

ここまでの例に従った場合、「(venv-llm) ユーザー名@コンピュータ名:~\$ 」になる。

## 8. 仮想環境のpipをアップグレード

```sh
python3 -m pip install --upgrade pip
```

# 9. 仮想環境を抜ける必要があるときは
```sh
deactivate
```

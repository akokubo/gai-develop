# Ollamaの使い方

## Ollama公式サイト
https://ollama.com/

## 公式に登録された大規模言語モデル
公式サイトの[Models](https://ollama.com/search)で検索できる。

例えば以下のような。
* [Meta LLaMa ３.2](https://ollama.com/library/llama3.2) 2GB
* [Google Gemma 2 日本語版](https://ollama.com/schroneko/gemma-2-2b-jpn-it) 2.8GB
* [Google Gemma 3](https://ollama.com/library/gemma3) 3.3GB

他にもたくさんあり、パソコンのスペック次第で、大きいものも使える。

## OllamaでLLMをダウンロード

Windowsでは「Ubuntu」、macOSでは「ターミナル」を起動。

とりあえず小さいGemma 3の少サイズモデルをダウンロード

```sh
ollama pull gemma3:1b-it-qat
```

## OllamaでLLMを起動
```sh
ollama run gemma3:1b-it-qat
```

起動したら、何か質問して応答を確認する。

チャットを終了するには以下のように打つ。
```sh
/bye
```

## OllamaにインストールされているLLMの一覧
```sh
ollama list
```

## Hugging Faceで公開された大規模言語モデル
GGUF形式で公開されているものが使える。

[使い方](https://note.com/schroneko/n/n6a7c34f0a50c)

例えば、以下のようなものがある。

* [DeepSeek R1 Qwen2.5 蒸留 Bakeneko 32B 日本語版のGGUF形式](https://huggingface.co/rinna/deepseek-r1-distill-qwen2.5-bakeneko-32b-gguf) 12GB

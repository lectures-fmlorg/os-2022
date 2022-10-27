# インフラ構築向けのデバッガー・チェッカー

## 導入方法

EC2 に SSH 後に以下のコマンドを実行してください。

### インストール

PIP インストールします。

```sh
$ pip3 install https://github.com/OHMORIYUSUKE/grech/blob/release/grech-0.1.0-py3-none-any.whl?raw=true
```

### 初期化

本演習向けの設定を入れます。

```sh
$ sudo grech config set https://raw.githubusercontent.com/lectures-fmlorg/os-2022/main/debugger/test.yml
```

### 設定

各自の環境で設定した情報を登録します。コマンドの指示に従って設定してください。

```sh
sudo grech config set
```

### チェック

演習すべての項目をチェックする。

※以降(インスタンスを停止しても)、このコマンドのみで確認することができます。

```sh
$ grech check all
```

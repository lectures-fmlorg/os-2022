# インフラ構築向けのデバッガー・チェッカー

## 導入方法

EC2 に SSH 後に以下のコマンドを実行してください。

### インストール

ツールをインストールします。PIP でインストールします。

```sh
$ sudo pip3 install https://github.com/OHMORIYUSUKE/grech/blob/release/grech-0.1.0-py3-none-any.whl?raw=true
```

### 初期化

本演習向けの設定を入れます。

```sh
$ sudo grech config set https://raw.githubusercontent.com/lectures-fmlorg/os-2022/main/debugger/test.yml
```

### 設定

各自の環境で設定した情報を登録します。コマンドの指示に従って設定してください。

- MySQL のユーザーには PHP からアクセスするユーザーを入力(ワークシート通りなら`root`)
- MySQL のパスワードは上記で設定したユーザーのパスワードを入力(各自設定したパスワード)

```sh
$ sudo grech config set
```

### チェック

演習すべての項目をチェックする。
すべてが緑色になれば設定が正しくされています。

> 動作を保証するものではありません。正常に動作するかは実際に試して確認してください。

※以降(インスタンスを停止しても)、このコマンドのみで確認することができます。

```sh
$ grech check all
```

#### すべてのテストが通った例

![](https://github.com/OHMORIYUSUKE/grech/raw/main/docs/images/all_1.png)

#### 結果の詳細

誤った設定を行っている場合は**コメント**の項目に赤でコメントされます。参考にして設定を修正してください。

## 詳細について

詳細の使い方については以下を参考にしてください。

https://github.com/OHMORIYUSUKE/grech

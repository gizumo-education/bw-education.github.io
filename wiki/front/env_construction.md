# フロントコース環境構築

フロントコースを受講するために必要なツールの導入を行なっていきます。  

## ツールのインストール

下記3つを順番にインストールしていきます。

- Homebrew(Macの方のみ)
- Volta
- Node.js

### Homebrew
※Windowsの方はHomebrewの設定は飛ばして、Voltaの設定に進んでください。  
HomebrewとはMacのためのパッケージ管理システムです。  
パッケージ管理システムとは、パッケージを一元管理し、管理を自動化するシステムのことを指します。

具体的にはHomebrewを使用することで、パッケージのインストールやアンインストール、バージョンの切り替えを簡単に行えるようになります。
それでは、Homebrewをインストールしていきましょう。

ターミナルを開いて下記のコマンドを実行してください。

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

しばらく待ってインストールが完了したら、下記のコマンドを実行しHomebrewがインストールされているか確認しましょう。

```shell
brew -v
```

下記のようにHomebrewのバージョンが表示されれば、Homebrewのインストールは完了です。

```shell
Homebrew 3.5.9
Homebrew/homebrew-core (git revision d1409ew; last commit 2022-08-22)
```

#### 「zsh: command not found: brew」が表示される場合
こちらのメッセージが表示された方は、追加で設定が必要なので下記コマンドを実行してください。  
※下記コマンドの「ユーザー名」の部分には自分のPCのユーザー名を入れてください。

```shell
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/ユーザー名/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
```

再度`brew -v`を実行してバージョンが表示されれば、Homebrewのインストールは完了です。

```shell
brew -v

Homebrew 3.5.9
Homebrew/homebrew-core (git revision d1409ew; last commit 2022-08-22)
```

### Volta
次にNode.jsやnpmのバージョンを管理してくれるVoltaをインストールします。  
VoltaもHomebrewで扱うことのできるパッケージなので、Homebrewを使用してインストールしていきます。(Windowsの方はPCに直接インストールします。)

#### Macの方
##### 1. インストールと確認
ターミナルで下記のコマンドを実行してください。

```shell
brew install volta
```

インストールが完了したら下記のコマンドを実行し、バージョンが表示されれば問題ありません。
```shell
volta -v

1.0.8
```

##### 2. 環境変数の設定
下記コマンドを実行してエラーなく処理が完了すれば問題ありません。

```shell
volta setup
```

##### 3. SHELLの再起動

```shell
exec $SHELL -l
```

##### 4. Nodeのインストールと確認

```shell
volta install node
```

下記コマンドを実行してバージョンが表示されれば完了です。

```shell
node -v

v16.17.0
```

#### Windowsの方

##### 1. 開発者モードをONにする
Voltaを使用するには、開発者モードをONに設定する必要があるので、下記手順で開発者モードをONにしてください。

1. 検索ボックスに「開発者」と入力し「開発者向け機能を使う」を起動
2. 開発者モードをONに変更

![開発者向け機能設定画面](https://res.cloudinary.com/gizumo-inc/image/upload/v1661313309/curriculums/Sass%20Lesson/developer_mode.png)

##### 2. Voltaのインストール
[Volta公式サイトのGetting Started](https://docs.volta.sh/guide/getting-started)から「download and run the Windows installer」のリンクをクリックし、インストーラーをダウンロードします。

![Volta公式サイトのインストーラーダウンロード画面](https://res.cloudinary.com/gizumo-inc/image/upload/v1661313322/curriculums/Sass%20Lesson/volta_installer.png)

ダウンロードしたインストーラーを起動したら、全て「Next」をクリックし、最後のページで「Install」をクリックしてください。

![Voltaインストール確認画面](https://res.cloudinary.com/gizumo-inc/image/upload/v1661313317/curriculums/Sass%20Lesson/volta_install.png)

インストールが完了したらコマンドラインを起動し、下記コマンドを実行してバージョンが表示されればVoltaのインストールは完了です。

```shell
volta -v

1.0.8
```

##### 3. Nodeのインストールと確認

```shell
volta install node
```

下記コマンドを実行してバージョンが表示されれば完了です。

```shell
node -v

v16.17.0
```

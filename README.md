# My DevEnv Playbook
自分用

### 現状の機能
- homebrew & homebrew_cask install
- nodebrew install & nodejs install
- npm global packages install
- font file setup

### 予定してる機能
- adk & adn 環境変数の設定
- atom editor の設定ファイルの自動配置
- $ nodebrew install [version] 時のエラーハンドリング
- vars: の利用の際に"bera valiables"と警告がでることへの対応

### Setup
1. Xcode & Command Line Tools の install
```
$ xcode-select --install
```
2. homebrew と ansible 、git をinstall
```
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
$ brew install ansible
$ brew install git
```
3. この playbook を git clone でダウンロード
```bash
$ git clone https://github.com/tomo3110/myLocalDevEnv.git
```
4. playbook を ダウンロードしたディレクトリへ移動
```
$ cd ./myLocalDevEnv
```
5. playbook を実行する
```
$ ansible-playbook localhost.yml -i hosts
```

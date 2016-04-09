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

### 導入されるパッケージ一覧
#### homebrew
- ansible
- nodebrew
- brew-cask
- git
- python
- android-sdk
- android-ndk

### brew-cask
- atom
- vagrant
- virtualbox
- google-chrome
- google-drive
<!-- - java  -->
- dropbox
- android-studio

### nodebrew
- v5.7.0

#### npm global
- electron-prebuild
- cordova
- react-native-cli
- webpack

#### atom editor packages
- atom-ternjs
- color-picker
- git-plus
- language-babel
- linter
- linter-eslint
- minimap
- minimap-git-diff
- project-manager
- terminal-plus
- editorconfig

#### font
- Ricty

### その他（雑感）
- roles > [各機能] > tasks 以外ほとんど使っていない。
- 導入部で git, ansible, homebrew を入れたならplaybookに要らないのでは？

などなど...

考え出すとキリがない。

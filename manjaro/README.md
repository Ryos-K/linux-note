# manjaro-note

Manjaro Linux に関するメモ

## 初期設定

### パッケージの更新

```sh
sudo pacman -Syu
```

### yay

```sh
sudo pacman -S base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

### 日本語入力

#### fcitx5, mozc

```sh
sudo pacman -S fcitx5-im fcitx-mozc
```

リポジトリの選択はデフォルトの all 

```.zshenv
#input method module setting
GTK_IM_MODULE="fcitx5"
QT_IM_MODULE="fcitx5"
XMODIFIERS='@im=fcitx5'
```

#### mozc の設定

```sh
/usr/lib/mozc/mozc_tool --mode=config_dialog
```

### Chrome

```
yay -S google-chrome
```

### Font

## 開発環境

### git

- ssh

```sh
cd ~/.ssh
ssh-keygen -t rsa
cat id_rsa.pub
```

- config

```sh
git config --global user.email "example@email.com"
git config --global user.name  "name"
```

### Terminal

### Vscode

### Android Studio

### Intellij Idea

### 言語

#### Java / Kotlin / Scala

- sdkman!

```
curl "https://get.sdkman.io" | bash
```

- java / kotlin / scala

```
sdk install java 17.0.7-tem
sdk install kotlin
sdk install scala
```

#### Python

#### Rust





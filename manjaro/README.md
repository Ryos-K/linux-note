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

## 開発環境

### Terminal

### Vscode

### Android Studio

### Intellij Idea

## ランタイム

### Java

### Python

### Rust

## Font



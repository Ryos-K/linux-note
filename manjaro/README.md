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

- PlemolJP

[https://github.com/yuru7/PlemolJP/releases]

```sh
unzip Downloads/PlemolJP_NF_vX.Y.Z
sudo mv PlemolJP_NF_vX.Y.Z /usr/share/fonts/PlemolJP_NF
```

### Shortcut

ショートカットがエディタと重複しないようにする

```sh
gsettings set org.gnome.desktop.wm.keybindings move-to-workspace-up "['<Super><Shift>Page_Up']"
gsettings set org.gnome.desktop.wm.keybindings move-to-workspace-down  "['<Super><Shift>Page_Down']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-down "['<Super><Shift>Page_Down']"
gsettings set org.gnome.desktop.wm.keybindings switch-to-workspace-up  "['<Super><Shift>Page_Up']"
```

Ctrl と Capslock を入れ替える

```sh
gsettings set org.gnome.desktop.input-sources xkb-options "['ctrl:swapcaps']"
```

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

```sh
sudo pacman -S guake
```

### VScode

```sh
yay -S visual-studio-code-bin
```

### Android Studio

[https://developer.android.com/studio]

```sh
sudo tar -xzf Downloads/android-studio-*-linux.tar.gz -C /opt
/opt/android-studio/bin/studio.sh
```

- USB Debug

```sh
sudo pacman -Syu android-udev android-tools
```

### Intellij Idea

[https://www.jetbrains.com/idea/download/download-thanks.html?platform=linux]

```sh
sudo tar -xzf -xzf Downloads/ideaIU-*.tar.gz -C /opt
/opt/idea-IU-*/bin/idea.sh
```

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





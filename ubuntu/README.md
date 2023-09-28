# ubuntu-note

Ubuntu に関するメモ

## 初期設定

### パッケージの更新

```sh
sudo apt update && sudo apt upgrade
```

### 日本語入力

#### fcitx5, mozc

```sh
sudo apt install fcitx5-mozc
```

```sh
sudo localectl set-locale LANG=C
```

```.zshenv
#input method module setting
GTK_IM_MODULE="fcitx5"
QT_IM_MODULE="fcitx5"
XMODIFIERS='@im=fcitx5'
```

- 起動時に fcitx5 が起動しない場合は Startup に登録する

### Chrome

[Chrome](https://www.google.com/chrome/?brand=YTUH&gclid=Cj0KCQjwpc-oBhCGARIsAH6ote9cTTOQ14Ay8xh9XnurtQNmQhvqzjX5_WZAK4_sBxHUK_rLmnbVsgUaAuySEALw_wcB&gclsrc=aw.ds)

### Shorcut

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

Capslock を Ctrl にする

```sh
gsettings set org.gnome.desktop.input-sources xkb-options "['ctrl:nocaps']"
```

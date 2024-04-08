# ukylin wine for Ubuntu

## 软件说明
> 本项目可以使用移植包在ubuntu上使用linux原生微信

## 一、项目介绍
> Ubuntu linux原生微信

> 仅在ubuntu20.04上测试过，不保证在其他系统上可用

## 二、使用介绍
> 下载微信到本地

[点击下载微信](https://github.com/web1n/wechat-universal-flatpak/releases/download/2403201255/com.tencent.WeChat.flatpak)
> 安装flatpak
```
sudo apt-get install flatpak
```
> 输入以下命令配置
```
sudo flatpak remote-add --if-not-exists --system flathub https://flathub.org/repo/flathub.flatpakrepo
```
> 安装微信
```
flatpak install com.tencent.WeChat.flatpak
```
> 复制图标
```
sudo cp /var/lib/flatpak/app/com.tencent.WeChat/current/active/export/share/applications/com.tencent.WeChat.desktop /usr/share/applications/
sudo cp -R /var/lib/flatpak/app/com.tencent.WeChat/current/active/export/share/icons/hicolor/* /usr/share/icons/hicolor/
```
> 给微信全部目录权限
```
sudo flatpak override com.tencent.WeChat --filesystem=home
```
> 重启电脑
## 三、感谢
[web1n/wechat-universal-flatpak](https://github.com/web1n/wechat-universal-flatpak)


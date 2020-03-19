# ติดตั้ง Linux Subsystem For Windows 10

{% embed url="https://medium.com/@themaxaboy/%E0%B9%80%E0%B8%95%E0%B8%A3%E0%B8%B5%E0%B8%A2%E0%B8%A1%E0%B8%95%E0%B8%B1%E0%B8%A7%E0%B8%81%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%AD%E0%B8%AD%E0%B8%81%E0%B9%80%E0%B8%94%E0%B8%B4%E0%B8%99%E0%B8%97%E0%B8%B2%E0%B8%87-macos-setup-%E0%B9%81%E0%B8%99%E0%B8%B0%E0%B8%99%E0%B8%B3%E0%B8%AA%E0%B8%B3%E0%B8%AB%E0%B8%A3%E0%B8%B1%E0%B8%9A-developer-169c06537d53" %}

{% embed url="https://www.sitepoint.com/zsh-tips-tricks/" %}

{% embed url="https://www.howtogeek.com/258518/how-to-use-zsh-or-another-shell-in-windows-10/" %}

{% embed url="https://medium.com/grean-developers-family/%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%A1%E0%B8%B1%E0%B8%99%E0%B8%95%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%A1%E0%B8%B5-%E0%B8%95%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B9%83%E0%B8%8A%E0%B9%89-z-shell-zsh-%E0%B8%84%E0%B8%A5%E0%B8%B9%E0%B9%86-%E0%B8%9A%E0%B8%99-windows-10-vscode-f5ba3a8dc493" %}

{% embed url="http://www.oopsbox.com/?p=220" %}

{% embed url="https://armno.in.th/2015/03/24/oh-my-zsh-to-prezto/" %}



## เปิด feature

![](.gitbook/assets/image%20%282%29.png)

## ติดตั้ง Ubuntu จาก Microsoft Store

![](.gitbook/assets/image%20%283%29.png)

## อัปเดต Ubuntu ให้เป็นเวอชั่นล่าสุด

{% embed url="https://opensource.cc.psu.ac.th/Update\_package\_%E0%B8%94%E0%B9%89%E0%B8%A7%E0%B8%A2\_apt-get" %}



```text
sed -i 's/\/us.archive/\/th.archive/g' /etc/apt/sources.list
หรือ /archive.ubuntu เป็น th.archive.ubuntu ดังนี้
sed -i 's/\/archive/\/th.archive/g' /etc/apt/sources.list

sudo apt-get update
```

## ติดตั้ง Zsh

```text
sudo apt-get install zsh

zsh --version

chsh -s /bin/zsh

whereis zsh
```










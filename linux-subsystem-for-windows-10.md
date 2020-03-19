# ติดตั้ง Linux Subsystem For Windows 10

{% embed url="https://medium.com/@themaxaboy/%E0%B9%80%E0%B8%95%E0%B8%A3%E0%B8%B5%E0%B8%A2%E0%B8%A1%E0%B8%95%E0%B8%B1%E0%B8%A7%E0%B8%81%E0%B9%88%E0%B8%AD%E0%B8%99%E0%B8%AD%E0%B8%AD%E0%B8%81%E0%B9%80%E0%B8%94%E0%B8%B4%E0%B8%99%E0%B8%97%E0%B8%B2%E0%B8%87-macos-setup-%E0%B9%81%E0%B8%99%E0%B8%B0%E0%B8%99%E0%B8%B3%E0%B8%AA%E0%B8%B3%E0%B8%AB%E0%B8%A3%E0%B8%B1%E0%B8%9A-developer-169c06537d53" %}

{% embed url="https://www.sitepoint.com/zsh-tips-tricks/" %}

{% embed url="https://www.howtogeek.com/258518/how-to-use-zsh-or-another-shell-in-windows-10/" %}

{% embed url="https://medium.com/grean-developers-family/%E0%B8%82%E0%B8%AD%E0%B8%87%E0%B8%A1%E0%B8%B1%E0%B8%99%E0%B8%95%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%A1%E0%B8%B5-%E0%B8%95%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B9%83%E0%B8%8A%E0%B9%89-z-shell-zsh-%E0%B8%84%E0%B8%A5%E0%B8%B9%E0%B9%86-%E0%B8%9A%E0%B8%99-windows-10-vscode-f5ba3a8dc493" %}



## เปิด feature

![](.gitbook/assets/image%20%282%29.png)

## ติดตั้ง Ubuntu จาก Microsoft Store

![](.gitbook/assets/image%20%283%29.png)

## อัปเดต Ubuntu ให้เป็นเวอชั่นล่าสุด

```text
sudo apt-get update
```

## ติดตั้ง Homebrew

{% embed url="https://docs.brew.sh/Homebrew-on-Linux" %}

```text
brew search <ชื่อโปรแกรม>          //ใช้ค้นหาโปรแกรมที่ต้องการลง
brew install <ชื่อโปรแกรม>         //ใช้ติดตั้งโปรแกรมที่แนว Command line
brew cask install <ชื่อโปรแกรม>    //ใช้ติดตั้งโปรแกรมที่มี UI
brew uninstall <ชื่อโปรแกรม>       //ใช้ถอนการติดตั้ง
brew list <ชื่อโปรแกรม>            //ใช้ดูโปรแกรมทั้งหมดที่ติดตั้งผ่าน brew
brew upgrade                     //ใช้อัพเดทโปรแกรมที่เรามีให้ใหม่ล่าสุด
```

```text
sudo apt install linuxbrew-wrapper

brew --help
```

```bash
Next steps:
- Install the Linuxbrew dependencies if you have sudo access:
  Debian, Ubuntu, etc.
    sudo apt-get install build-essential
  Fedora, Red Hat, CentOS, etc.
    sudo yum groupinstall 'Development Tools'
  See http://linuxbrew.sh/#dependencies for more information.
- Add Linuxbrew to your ~/.bash_profile by running
    echo 'export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"' >>~/.bash_profile
    echo 'export MANPATH="/home/linuxbrew/.linuxbrew/share/man:$MANPATH"' >>~/.bash_profile
    echo 'export INFOPATH="/home/linuxbrew/.linuxbrew/share/info:$INFOPATH"' >>~/.bash_profile
- Add Linuxbrew to your PATH
    PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"
- We recommend that you install GCC by running:
    brew install gcc
- Run `brew help` to get started
- Further documentation:
    http://docs.brew.sh
Warning: /home/linuxbrew/.linuxbrew/bin is not in your PATH.
/usr/bin/brew: 78: exec: /home/diversition/.linuxbrew/bin/brew: not found
```

## ติดตั้ง font

```text
brew tap homebrew/cask-fonts 
brew cask install font-cascadia
```

## ติดตั้ง Zsh

```text
brew install zsh
```








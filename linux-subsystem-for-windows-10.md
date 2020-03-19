# ติดตั้ง Linux Subsystem For Windows 10

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








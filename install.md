## Add 3rd party package repositories
```bash
echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-stretch-prod stretch main" > /etc/apt/sources.list
echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" >> /etc/apt/sources.list
echo "deb http://ftp.de.debian.org/debian stretch main " >> /etc/apt/sources.list
echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list
curl https://packages.microsoft.com/keys/microsoft.asc | apt-key add -
apt-get update
apt -y install curl gnupg apt-transport-https
```

## Install Powershell
```bash
apt install powershell
```

https://www.netsecfocus.com/infosec/tools/2017/09/25/Installing_Powershell_and_Powershell_Preview_on_Kali_Linux_2018-3.html

## Install Mono / MonoDevelop
```bash
apt install mono-devel
apt install monodevelop
```

## Install VSCode
```bash
apt install code
mkdir /root/code
```

## Install dotnet 
todo: check what repo this comes from
```bash
apt install dotnet-sdk-2.2
```

## Install Discord
```bash
wget -O discord.deb "https://discordapp.com/api/download?platform=linux&format=deb"
apt-get install ./discord.deb
```

## Using built in chromium and installing Google Chrome
you can run chromium on kali by typing ``chromium --no-sandbox`` in the run dialog. Using the default shortcuts built in will fail when running as root due to the nature of chrome wanting to not run as root! I would like to iterate that this is a horrible idea, but, lets do it anyways. 

Why not just run firefox? 
mainly just because firefox doesn't handle the touch screen well.

```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
apt install ./google-chrome-stable_current_amd64.deb 
```

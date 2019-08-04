## Add 3rd party package repositories
```bash
echo "deb [arch=amd64] https://packages.microsoft.com/repos/microsoft-debian-stretch-prod stretch main" > /etc/apt/sources.list
echo "deb http://http.kali.org/kali kali-rolling main non-free contrib" >> /etc/apt/sources.list
echo "deb http://ftp.de.debian.org/debian stretch main " >> /etc/apt/sources.list
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
apt-install mono-devel
apt-install mono-develop
```

##Installing dotnet 
todo: check what repo this comes from
```bash
apt install dotnet-sdk-2.2
```

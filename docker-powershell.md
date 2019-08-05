#Powershell NTLM

## Docker On Kali
https://medium.com/@airman604/installing-docker-in-kali-linux-2017-1-fbaa4d1447fe

```bash
curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
echo 'deb [arch=amd64] https://download.docker.com/linux/debian buster stable' > /etc/apt/sources.list.d/docker.list
apt-get update
apt-get install docker-ce
```

## Test It
```bash
docker run hello-world
```

## Get Powershell NTLM
```bash
docker pull quickbreach/powershell-ntlm
```

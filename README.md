# Ubuntu ecCodes prebuild ubuntu packages

Ubuntu 22.04 (jammy) prebuild amd64 libeccodes0 packages

```bash
wget -qO - https://patrick-zippenfenig.github.io/ecCodes-ubuntu/public.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/ecCodes-ubuntu.gpg > /dev/null

echo "deb https://patrick-zippenfenig.github.io/ecCodes-ubuntu/ jammy main" | sudo tee /etc/apt/sources.list.d/ecCodes-ubuntu.list2

sudo apt update
sudo apt install libeccodes0
```
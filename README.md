# ecCodes ubuntu packages

Prebuilt eccodes packages for Ubuntu 22.04 (jammy) amd64 and hosted as an APT repository on GitHub pages. Used for the open source weather api https://open-meteo.com

```bash
wget -qO - https://patrick-zippenfenig.github.io/ecCodes-ubuntu/public.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/ecCodes-ubuntu.gpg > /dev/null

echo "deb https://patrick-zippenfenig.github.io/ecCodes-ubuntu/ jammy main" | sudo tee /etc/apt/sources.list.d/ecCodes-ubuntu.list

sudo apt update
sudo apt install openmeteo-eccodes
```
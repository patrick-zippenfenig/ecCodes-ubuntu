# ecCodes ubuntu packages

Prebuilt eccodes packages for Ubuntu 22.04 (jammy) and hosted as an APT repository on GitHub pages. Supports amd64 and arm64.

Used to get the latest ECMWF eccodes library for the open source weather api https://open-meteo.com

```bash
curl -L https://patrick-zippenfenig.github.io/ecCodes-ubuntu/public.key | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/ecCodes-ubuntu.gpg > /dev/null

echo "deb https://patrick-zippenfenig.github.io/ecCodes-ubuntu/ jammy main" | sudo tee /etc/apt/sources.list.d/ecCodes-ubuntu.list

sudo apt update
sudo apt install openmeteo-eccodes
```


Notes: Testing on macos arm
```bash
docker run -it --security-opt seccomp=unconfined --platform linux/amd64 ubuntu
apt update
apt install curl gpg sudo
```
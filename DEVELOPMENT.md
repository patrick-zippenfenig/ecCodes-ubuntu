# Development notes

Notes: Testing on macos arm
```bash
docker run -it --security-opt seccomp=unconfined --platform linux/amd64 ubuntu
apt update
apt install curl gpg sudo
```
---
layout: home
title: Comexr repo
---
This repository provides the following packages:
- [lwl-drivers](https://github.com/comexr/lwl-drivers)
- [yt6801 - ethernet drivers] (https://github.com/comexr/yt6801)
Instructions to install these are on the corresponding pages.

## Add repository

### Debian/Ubuntu(-based)
Import the [public key](comexr.asc):
```
wget -qO- {{ site.url }}/comexr.asc | sudo tee /etc/apt/keyrings/comexr.asc >/dev/null
```
Add the repository:
```
echo "deb [arch=all signed-by=/etc/apt/keyrings/comexr.asc] {{ site.url }}/deb stable main" | sudo tee /etc/apt/sources.list.d/comexr.list >/dev/null
```
Install the desired packages:
```
sudo apt update
sudo apt install -y <packages>
```

### Fedora
Import the [public key](comexr.asc):
```
sudo rpm --import {{ site.url }}/comexr.asc
```
Add the repository:
```
sudo dnf config-manager --add-repo {{ site.url }}/comexr.repo
```
Install the desired packages:
```
sudo dnf install -y <packages>
```

### OpenSUSE
Import the [public key](comexr.asc):
```
sudo rpm --import {{ site.url }}/comexr.asc
```
Add the repository:
```
sudo zypper addrepo {{ site.url }}/comexr.repo
```
Install the desired packages:
```
sudo zypper in -y <packages>
```

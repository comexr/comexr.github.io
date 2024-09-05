---
layout: home
title: Comexr Website
---
This repository provides the following packages:
- [lwl-drivers](https://github.com/comexr/lwl-drivers)

## Add repository

### Debian/Ubuntu(-based)
Import the [public key](comexr.asc):
```
wget -qO- {{ site.url }}/comexr.asc | sudo tee /etc/apt/keyrings/comexr.asc >/dev/null
```

Add the source to `/etc/apt/sources.list.d/`:
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
sudo rpmkeys --import {{ site.url }}/comexr.asc
```
Download the repo file:
```
curl {{ site.url }}/comexr.repo
```

Install the desired packages:
```
sudo dnf install -y <packages>
```

### OpenSUSE

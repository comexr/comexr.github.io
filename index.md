---
layout: home
title: Comexr repo
---
This repository provides the following packages:
- [lwl-drivers](https://github.com/comexr/lwl-drivers)

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
sudo rpmkeys --import {{ site.url }}/comexr.asc
```
Add the repository:
```
printf "[{{ site.title }}]\nname={{ site.title }} Repo\nbaseurl={{ site.url }}/rpm\nenabled=1\ngpgcheck=1\nrepo_gpgcheck=1\ngpgkey={{ site.url }}/{{ site.title }}.asc" | sudo tee -a /etc/yum.repos.d/comexr.repo
```
Install the desired packages:
```
sudo dnf install -y <packages>
```

### OpenSUSE
Import the [public key](comexr.asc):
```
sudo rpmkeys --import {{ site.url }}/comexr.asc
```
Add the repository:
```
printf "[{{ site.title }}]\nname={{ site.title }} Repo\nbaseurl={{ site.url }}/rpm\nenabled=1\ngpgcheck=1\nrepo_gpgcheck=1\ngpgkey={{ site.url }}/{{ site.title }}.asc" | sudo tee -a /etc/zypp/repos.d/comexr.repo
```
Install the desired packages:
```
sudo zypper in -y <packages>
```
